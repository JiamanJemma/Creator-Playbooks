# 配图生成 & 审美 Playbook

## ⚠️ 长文配图（强制前置）
如果是为**长文/文章**生成配图，按照你自己的长文配图审美要求。本文件只提供通用审美偏好，不替代长文配图流程。

## 配图风格（必须遵守）

**统一：泥塑风 + 白色背景 + 淡紫色**

- 白色背景，干净清爽有呼吸感
- 泥塑3D元素，圆鼓鼓软萌有光泽
- 淡紫色主色调（薰衣草紫 #ede9fe）
- **画多字少**，英文prompt生成
- 署名：`<YOUR_IP_NAME> · <YOUR_WEBSITE>`

**禁止：** 深色背景、字太多、写实/扁平风、图上叠加中文小字

## 配图尺寸

| 平台 | 尺寸 |
|------|------|
| 小红书/抖音封面 | portrait 竖图 3:4 |
| X/Twitter | landscape 横图 |
| Instagram | 1:1 方图 |
| YouTube/B站封面 | 16:9 |
| B站封面 | 4:3 |

## 分工

- **generate_image** → 灵感配图、封面（直接生成，无水印）
- **NotebookLM CLI** → 信息图（复杂内容）
- **Midjourney** → 高质感特殊配图（佳蔓有会员）

## 泥塑 IP 角色 Prompt

```
Play-Doh plasticine clay figurine, young Chinese woman, long straight black hair, pinkish-brown thin frame glasses on top of head, lilac purple turtleneck sweater, high-waisted cream wide-leg pants, white sneakers, [动作/场景], white background, soft clay texture, soft lighting, ultra high resolution
```

## 审美偏好

给配色/排版建议时直接给具体值，不说废话：
- 淡色系：薰衣草紫 #ede9fe、樱花粉 #fce7f3、薄荷绿 #d1fae5、蜜桃黄 #fef3c7、天空蓝 #e0e7ff
- 鲜艳系（需醒目时）：蓝 #6B8AFF、红 #FF4D7A、绿 #2ED8A0、黄 #FFAA22、紫 #B799FF
- 风格：简洁有呼吸感、可爱不幼稚、知性温柔、大留白
- 禁止：深色系、过度装饰、字体混乱

## 封面 3D 字体资产专用 Prompt
生成封面大字大标题时（需方便抠图、抗发光描边、高对比度），**必须强制使用**以下款式（正面纯白+粗深紫厚底+平视无阴影）：
```
Play-Doh plasticine clay 3D typography of the word '[文本内容]'. The front flat face of each letter is pure white. The thick 3D puffy outline and extruded sides of the letters are a deep dark violet purple. Straight-on direct frontal view. Pure solid #FFFFFF white background. High contrast, fully isolated sticker style with ZERO drop shadows. Soft clay texture, flat bright lighting, clean cutout perfectly suited for chroma keying.
```
