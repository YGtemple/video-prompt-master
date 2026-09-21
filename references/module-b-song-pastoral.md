---
name: song-pastoral-mj-seedance
description: 宋式田园水乡生活图片提示词（MJ V8）+ 成图后4秒视频提示词（Seedance 2.5）
---

# 宋式田园美学 · 图片到视频

把用户已认可的两条提示词当作可复制的文字模板。图片阶段用纯文字先生成生活瞬间，成图阶段再根据实际画面写动作。

## 阶段与默认值

- 图片阶段：默认10张独立英文提示词，每条50-80个英文词，默认 `--ar 16:9 --v 8.2 --raw`。
- 视频阶段：用户上传成图后，一图一条中文Seedance 2.5提示词，约4秒、单个连续镜头。
- 未指定人物时，使用清秀亲切的年轻成年中国女子，黑色长发半束或简单扎起，素净日常衣裙。

## 两条认可原文：不可改写的基准

### A｜溪边浣衣
```text
Beside a clear village stream, one young adult Chinese woman kneels on a flat stone, both hands twisting wet linen above a wooden basin, watching falling droplets with a gentle smile. Black hair tied back, pale blue cotton Song-style wrap blouse, closed collar, rolled sleeves, ivory skirt. Medium-wide composition includes face, hands, basin and supporting knees. Clear daylight, warm highlights, green water reflections, photoreal pastoral film still. --ar 16:9 --v 8.2 --raw
```

### B｜墙头摘果
```text
Leaning over a village courtyard wall, a young adult Chinese woman picks a low yellow fruit, left palm braced on the tiles, right fingers holding its stem. She watches the fruit with a small, playful smile. Long black hair half-tied, plain peach cotton wrap blouse, neatly crossed collar, ivory skirt. Medium shot includes both hands and the wall. Gentle dappled daylight, natural skin tones, softly receding green foliage. Photoreal pastoral film still. --ar 16:9 --v 8.2 --raw
```

## 图片阶段：严格按槽位迁移

**A模板（水边、舟中、洗涤、采莲等）：**
```text
[地点], one young adult Chinese woman [动作], [身体支撑], [道具]. Black hair tied back, pale blue cotton Song-style wrap blouse, closed collar, rolled sleeves, ivory skirt. Medium-wide composition includes face, hands, [道具] and supporting [支撑]. Clear daylight, warm highlights, green water reflections, photoreal pastoral film still. --ar 16:9 --v 8.2 --raw
```

**B模板（院落、树下、陆地活动等）：**
```text
[地点], a young adult Chinese woman [动作], [身体支撑], [道具]. She watches [对象] with a small, playful smile. Long black hair half-tied, plain peach cotton wrap blouse, neatly crossed collar, ivory skirt. Medium shot includes both hands and [生活空间]. Gentle dappled daylight, natural skin tones, softly receding green foliage. Photoreal pastoral film still. --ar 16:9 --v 8.2 --raw
```

### 槽位规则

1. **先写事情，再写人。** 动作必须能看见接触关系。
2. **保持人物称呼。** 用 `young adult Chinese woman`。
3. **保持发型衣着。** A使用浅蓝棉质交领上衣；B使用素色桃粉棉质交领上衣。
4. **保持中景可读。** 画面要看见脸、双手、工具和支撑点。
5. **保持一件事。** 一条图片提示词只定格一个动作。
6. **保持光色原句。** 不随意改写。
7. **限制环境修饰。** 不堆叠bokeh、胶片、8K等。
8. **词数优先。** 超过80词删重复，少于50词补可见道具。

### 禁止词

`cinematic`、`moody`、`golden hour`、`sunset`、`dramatic lighting`、`fashion editorial`、`portrait`、`close-up`、`low angle`、`beautiful woman`、`luminous skin`、`flowing sleeves`、`airy gauze`、`letterbox`。

## 视频阶段：以成图为准

先逐张看成图，记录实际人物数量、发型衣着、脸朝向、手与道具接触、身体支撑、光向、画幅和可运动空间。每条约4秒只安排一个主要动作。

交付格式为"图片01｜主题｜约4秒"，随后一个中文 `text` 代码块，通常150-250字。一图一镜，不切镜、不转场、不黑场收尾。