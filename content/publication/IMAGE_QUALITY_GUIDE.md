# 提高 Featured 图片显示质量的完整指南

## 🎯 已完成的优化

1. **提高图片质量设置**
   - 已将 `config.yaml` 中的 `quality` 从 75 提升到 95
   - 使用 `lanczos` 重采样滤镜（最高质量）

2. **优化焦点设置**
   - 已设置 `focal_point: 'Smart'` 自动检测图片重要区域

## 📸 获得最佳显示效果的建议

### 1. 源图片要求

**推荐规格**：
- **分辨率**: 1920 x 1080 像素或更高（16:9 比例）
- **格式**: PNG（无损）或高质量 JPG
- **文件大小**: 1-3 MB（不要过度压缩）
- **DPI**: 至少 150 DPI，推荐 300 DPI

**最小规格**：
- **分辨率**: 1200 x 675 像素
- **格式**: JPG 或 PNG
- **文件大小**: 500 KB - 2 MB

### 2. 图片格式选择

| 格式 | 优点 | 缺点 | 推荐用途 |
|------|------|------|----------|
| **PNG** | 无损压缩，清晰度高 | 文件较大 | 图表、框架图、包含文字的图片 |
| **JPG** | 文件较小 | 有损压缩 | 照片、色彩丰富的图片 |
| **WebP** | 压缩率高且质量好 | 浏览器兼容性 | 现代浏览器的最佳选择 |

**对于学术论文图片，强烈推荐使用 PNG 格式！**

### 3. 从论文中导出高质量图片

#### 方法 A: 从 PDF 导出
如果你的论文是 PDF 格式：

1. **使用 Adobe Acrobat**:
   - 工具 → 导出 PDF → 图像 → PNG
   - 设置分辨率为 300 DPI 或更高

2. **使用 Inkscape**（免费）:
   - 打开 PDF
   - 选择图片
   - 文件 → 导出 PNG → 设置 DPI 为 300

3. **使用 GIMP**（免费）:
   - 打开 PDF，选择导入分辨率 300 DPI
   - 裁剪所需图片
   - 导出为 PNG

#### 方法 B: 从源文件重新生成
最佳方式：使用原始的矢量图文件（如 .ai, .svg, .eps）重新导出

- **Illustrator**: 导出为 PNG，分辨率 300 DPI
- **PowerPoint/Keynote**: 另存为图片，选择最高质量
- **Python/Matplotlib**: 
  ```python
  plt.savefig('featured.png', dpi=300, bbox_inches='tight')
  ```
- **R/ggplot2**:
  ```r
  ggsave("featured.png", width=12, height=6.75, dpi=300)
  ```

### 4. 图片优化流程

#### 步骤 1: 准备高质量源图片
- 使用上述方法导出 300 DPI 的 PNG 图片
- 确保图片尺寸至少 1920 x 1080 像素

#### 步骤 2: 适当裁剪
- 移除多余的空白边距
- 保持 16:9 的宽高比（如 1920x1080, 1600x900）
- 确保关键内容在中央区域

#### 步骤 3: 优化但不过度压缩
使用图片编辑工具：

**在线工具**:
- [TinyPNG](https://tinypng.com/) - 智能压缩，质量损失小
- [Squoosh](https://squoosh.app/) - Google 开发，可调整参数

**设置建议**:
- PNG: 不需要额外压缩，直接使用
- JPG: 质量设置为 90-95%

#### 步骤 4: 命名并放置
```
content/publication/TRAFICA/
├── index.md
├── cite.bib
└── featured.png  ← 高质量图片放这里
```

### 5. 配置文件检查清单

#### config.yaml
```yaml
imaging:
  resampleFilter: lanczos  # 最高质量的重采样
  quality: 95              # 已优化到 95
  anchor: smart            # 智能裁剪
```

#### index.md
```yaml
image:
  caption: 'TRAFICA framework'
  focal_point: 'Smart'     # 或 'Center'
  preview_only: false
```

### 6. 清除缓存

修改配置后，需要清除 Hugo 的图片缓存：

```bash
# 删除 resources 文件夹
rm -rf resources/_gen

# 或者使用 hugo 命令清理
hugo --gc
```

然后重新构建网站。

### 7. Netlify 特定设置

如果你在 Netlify 上部署，检查 `netlify.toml`:

```toml
[build]
  command = "hugo --gc --minify -b $URL"
  publish = "public"

[build.environment]
  HUGO_VERSION = "0.111.3"
  HUGO_ENV = "production"
  HUGO_ENABLEGITINFO = "true"
```

### 8. 常见问题排查

#### 问题 1: 图片仍然模糊
**解决方案**:
1. 检查源图片是否足够清晰（至少 1200x675）
2. 确保使用 PNG 格式而不是 JPG
3. 清除缓存并重新构建

#### 问题 2: 图片显示不完整
**解决方案**:
- 调整 `focal_point` 设置
- 尝试不同的值：`Smart`, `Center`, `Top`, `Bottom`

#### 问题 3: 图片文件太大
**解决方案**:
- 使用 TinyPNG 或 Squoosh 压缩
- 目标：1-2 MB 对于 PNG，500KB-1MB 对于 JPG

#### 问题 4: 图片加载慢
**解决方案**:
- 考虑使用 WebP 格式
- 使用适当的压缩（不要过度）
- 确保图片尺寸不超过 2000x1125

### 9. 推荐工具

#### 图片编辑
- **GIMP** (免费) - 功能强大
- **Photoshop** - 专业工具
- **Affinity Photo** - 性价比高

#### 图片压缩
- **TinyPNG** - PNG 压缩
- **Squoosh** - 多格式支持
- **ImageOptim** (Mac) - 批量优化

#### 格式转换
- **CloudConvert** - 在线转换
- **XnConvert** - 批量转换

### 10. 最佳实践总结

✅ **DO（推荐做法）**:
- 使用至少 1920x1080 的高分辨率图片
- 对于包含文字的图片使用 PNG 格式
- 保持 16:9 的宽高比
- 图片质量设置为 90-95
- 定期清除 Hugo 缓存

❌ **DON'T（避免做法）**:
- 不要使用低于 1200x675 的图片
- 不要过度压缩图片（质量 < 85）
- 不要使用截图而不是原始图片
- 不要忘记清除缓存

### 11. 快速检查命令

在终端运行以下命令检查图片信息：

```bash
# 检查图片尺寸
file featured.png

# 检查图片详细信息（需要 ImageMagick）
identify -verbose featured.png

# 查看图片文件大小
ls -lh featured.png
```

### 12. 示例：完美的 Featured 图片配置

```yaml
# 在 index.md 中
image:
  caption: 'TRAFICA: Open Chromatin Language Model Framework'
  focal_point: 'Smart'
  preview_only: false
  alt_text: 'TRAFICA framework architecture diagram'
```

**配套图片规格**:
- 文件名: `featured.png`
- 尺寸: 1920 x 1080 像素
- 格式: PNG（24-bit 或 32-bit）
- 文件大小: 1.5 MB
- DPI: 300

---

## 🚀 立即行动

1. ✅ 已将图片质量提升到 95
2. ✅ 已设置 Smart 焦点
3. 📝 准备高质量的 featured.png（1920x1080, PNG 格式）
4. 📂 放置到 `content/publication/TRAFICA/` 文件夹
5. 🗑️ 清除缓存：`rm -rf resources/_gen`
6. 🔨 重新构建：`hugo --gc`
7. 🌐 部署到 Netlify

完成这些步骤后，你的 featured 图片会以最高质量显示！
