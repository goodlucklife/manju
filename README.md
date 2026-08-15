# 《误入仙门的最后魔女》GitHub 图片上传包

把本目录中的 `assets/images/` 上传到一个公开 GitHub 仓库后，即可用 raw 链接给小裴视频模型调用。

## 上传方式

1. 新建一个 public repo，例如 `last-witch-assets`。
2. 把本目录里的 `assets/` 文件夹上传到仓库根目录。
3. 使用 raw 链接格式：

```text
https://raw.githubusercontent.com/<你的用户名>/<仓库名>/main/assets/images/<文件名>
```

如果你的默认分支叫 `master`，把链接里的 `main` 改成 `master`。

## 小裴常用字段

### `sd-720满血-不卡脸（按次）` 首帧

```json
{
  "model": "sd-720满血-不卡脸（按次）",
  "prompt": "你的提示词",
  "seconds": "15",
  "aspect_ratio": "9:16",
  "resolution": "720p",
  "first_frame_url": "https://raw.githubusercontent.com/<你的用户名>/<仓库名>/main/assets/images/C01_suli_v1.png"
}
```

### `sd-720满血-不卡脸（按次）` 多参考图

```json
{
  "model": "sd-720满血-不卡脸（按次）",
  "prompt": "你的提示词",
  "seconds": "15",
  "aspect_ratio": "9:16",
  "resolution": "720p",
  "reference_image_urls": [
    "https://raw.githubusercontent.com/<你的用户名>/<仓库名>/main/assets/images/C01_suli_v1.png",
    "https://raw.githubusercontent.com/<你的用户名>/<仓库名>/main/assets/images/C02_guchangyuan_v1.png",
    "https://raw.githubusercontent.com/<你的用户名>/<仓库名>/main/assets/images/L01_cloud_plaza_v1.png"
  ]
}
```

## 检查

raw 链接必须在浏览器无登录状态下直接打开图片。如果打开的是 GitHub 网页预览，而不是图片文件本身，小裴可能读不到。
