# 闲鱼海报提示词生成器 (xianyu-poster-prompt)

为闲鱼（Xianyu）二手交易平台的产品设计海报**图片生成提示词**的 skill。

## 文件结构

```
xianyu-poster-prompt/
├── SKILL.md                          # 主入口：工作流程、风格库、输出模板
├── README.md                         # 本文件
├── evals/
│   └── evals.json                    # 测试用例
├── references/
│   ├── style-guide.md                # 9 种风格详细指南 + 决策树
│   └── prompt-templates.md           # 10 大品类 prompt 模板
└── xianyu-poster-prompt-workspace/   # 评测工作区
```

## 何时使用

当用户需要：
- 在闲鱼卖闲置商品，想做卖货图
- 转卖二手物品，想让物品照片更好看
- 生成产品海报的 AI 绘图提示词
- 给二手物品配宣传图
- 任何"产品 + 海报 + AI prompt"相关需求

## 使用方法

直接用自然语言告诉 Claude：
- "我想在闲鱼上卖一台 X100V 相机，帮我做海报"
- "我的 ZARA 风衣想转卖，能给个 ins 风的图片 prompt 吗"
- "闲鱼转卖正山小种茶叶礼盒，要国潮风"

Claude 会自动分析产品、推荐风格、生成 3 套不同的提示词方案。

## 输出

3 套不同侧重的海报方案，每套包含：
- 标题文案（闲鱼标题公式）
- 配色、字体、构图建议
- 英文 prompt（主要）
- 中文 prompt 补充
- Negative prompt
- 参数建议（宽高比、风格强度）
- 闲鱼合规提醒

## 核心原则

1. **真实感 > 精美**：闲鱼用户对棚拍白底图本能戒备
2. **避免商家特征**：不模仿淘宝、天猫的促销风格
3. **强调个人气质**：生活场景、自用故事、情感钩子
4. **合规第一**：不出现站外引流、极限词、违禁暗示

## 支持的绘图工具

- Midjourney
- 即梦 / 通义万相 / 文心一格（中文友好）
- Stable Diffusion (SD/SDXL)
- 其他通用 prompt