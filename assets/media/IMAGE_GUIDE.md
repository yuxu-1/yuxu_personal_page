# 网站图片使用完全指南

## 📁 图片存放位置

### 1. 相册图片 (Gallery)
**位置**: `/assets/media/albums/[相册名称]/`
**用途**: 展示研究活动、会议、团队照片等
**示例**: `/assets/media/albums/research/photo1.jpg`

### 2. 静态图片
**位置**: `/static/uploads/`
**用途**: 文章中的图片、图表、简历等
**示例**: `/static/uploads/figure1.png`

### 3. 个人头像
**位置**: `/content/authors/yuxu/avatar.jpg`
**用途**: 个人资料页面的头像

### 4. 背景图片
**位置**: `/assets/media/`
**用途**: 网站背景、hero banner等

---

## 🖼️ 如何在不同地方使用图片

### 方法1: Gallery 相册展示（已启用）

在主页显示图片相册，图片会以网格形式展示，点击可查看大图。

**步骤**:
1. 将图片放到 `/assets/media/albums/research/`
2. 图片会自动显示在主页的 Gallery 部分

**创建多个相册**:
```yaml
# 在 content/_index.md 中添加
  - block: markdown
    id: gallery-conferences
    content:
      title: Conference Photos
      subtitle: ''
      text: |-
        {{< gallery album="conferences" >}}
    design:
      columns: '1'
```

### 方法2: 在文章中插入图片

如果你要在博客文章或项目页面中插入图片：

**Markdown 语法**:
```markdown
![图片描述](/uploads/figure1.png)
```

**HTML 语法**:
```html
<img src="/uploads/figure1.png" alt="图片描述" width="80%">
```

### 方法3: 使用 Figure shortcode

更专业的图片展示方式，支持标题和说明：

```markdown
{{< figure src="uploads/figure1.png" title="研究成果" caption="这是图片说明文字" >}}
```

### 方法4: 并排显示多张图片

```markdown
{{< gallery album="research" >}}
```

---

## 📊 项目展示中的图片

在 `/content/project/` 下的项目中添加图片：

1. 在项目文件夹中放置 `featured.jpg` 作为封面图
2. 其他图片放在项目文件夹中，在 `index.md` 里引用

示例结构：
```
content/project/my-research/
├── index.md
├── featured.jpg  # 项目封面图
└── figure1.png   # 项目内容图
```

在 `index.md` 中引用：
```markdown
![实验结果](figure1.png)
```

---

## 🎨 图片优化建议

### 尺寸建议
- **Gallery相册**: 1200-2000px 宽
- **文章插图**: 800-1200px 宽
- **头像**: 400-600px 正方形
- **项目封面**: 1200x675px (16:9比例)

### 文件大小
- 尽量压缩到 500KB 以下
- 使用在线工具: TinyPNG, Squoosh.app

### 格式选择
- 照片: JPG
- 图表/截图: PNG
- 动画: GIF (小尺寸) 或 MP4
- 现代浏览器: WebP

---

## 🚀 快速开始示例

### 示例1: 添加研究活动照片

1. 将照片 `lab_meeting_2024.jpg` 复制到:
   `/assets/media/albums/research/`

2. 照片会自动显示在主页 Gallery 部分

### 示例2: 在出版物中添加图表

1. 将图表 `methodology.png` 复制到:
   `/static/uploads/`

2. 在出版物的 `index.md` 中添加:
   ```markdown
   ![研究方法](/uploads/methodology.png)
   ```

### 示例3: 创建会议照片相册

1. 创建文件夹:
   `/assets/media/albums/conferences/`

2. 放入会议照片

3. 在 `content/_index.md` 的合适位置添加:
   ```yaml
   - block: markdown
     id: conferences
     content:
       title: Academic Conferences
       subtitle: ''
       text: |-
         {{< gallery album="conferences" >}}
     design:
       columns: '1'
   ```

---

## ⚠️ 注意事项

1. **文件命名**: 使用英文字母、数字、连字符，避免空格和中文
2. **版权**: 确保你有权使用这些图片
3. **隐私**: 不要上传包含敏感信息的图片
4. **备份**: 保留原始高清图片的备份

---

## 🔗 相关文档

- Wowchemy Gallery: https://wowchemy.com/docs/content/writing-markdown-latex/#gallery
- Hugo Image Processing: https://gohugo.io/content-management/image-processing/
