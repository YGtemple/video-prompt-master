# 视频提示词生成大师 (video-prompt-master)

四大专业视频提示词生成模块整合包。

## 模块概览

| 模块 | 名称 | 输入 | 输出 |
|------|------|------|------|
| A | 电商TVC广告 | 产品参考图 | 30秒 Seedance 2.5 广告片提示词 |
| B | 宋式田园美学 | 一句话主题 | 10组 MJ V8 图片提示词 + 4秒视频提示词 |
| C | 中式诗意巨物美学 | 一句话/参考图 | MJ V8 图片提示词 + 4秒视频提示词 |
| D | AI高燃打斗 | 一句话打斗类型 | 30秒打斗分镜提示词 |

## 安装

```bash
git clone https://github.com/YGtemple/video-prompt-master.git
cp -r video-prompt-master /path/to/your/skills/
```

## 使用

直接描述你的需求，技能会自动路由到对应模块：

- "帮我给这个产品做个广告" → 模块A
- "写一组宋式田园生活的提示词" → 模块B
- "生成一个巨物仙境的图" → 模块C
- "写一段武侠打斗的提示词" → 模块D

## 技术栈

- Midjourney V8.2
- Seedance 2.5
- 图片→视频两阶段工作流

## License

MIT
