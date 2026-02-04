# 图片相册使用说明

## 如何添加图片

1. 将你的图片文件放到这个文件夹中：
   `/assets/media/albums/research/`

2. 支持的图片格式：
   - JPG/JPEG
   - PNG
   - GIF
   - WebP

3. 建议的图片命名：
   - 使用英文字母和数字
   - 例如：lab_meeting_2024.jpg, conference_poster.png

## 如何创建多个相册

1. 在 `/assets/media/albums/` 下创建新文件夹，例如：
   - `research` - 研究活动照片
   - `conferences` - 会议照片
   - `team` - 团队照片
   - `awards` - 获奖照片

2. 在 `content/_index.md` 中添加新的 gallery 块：

```yaml
  - block: markdown
    id: conferences
    content:
      title: Conference Gallery
      subtitle: 'Academic Conferences'
      text: |-
        {{< gallery album="conferences" >}}
    design:
      columns: '1'
```

## 图片尺寸建议

- 宽度：建议 1200-2000 像素
- 高度：建议 800-1500 像素
- 文件大小：建议小于 2MB 以保证加载速度

## 示例

将你的图片（如 `lab_photo_2024.jpg`）放到这个文件夹中，它会自动显示在网站的 Gallery 部分。
