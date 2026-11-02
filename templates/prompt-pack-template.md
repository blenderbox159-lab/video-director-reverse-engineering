# Prompt Pack Template

# AI 视频生成提示词包模板


## Purpose

用于将导演逆向工程分析结果，

转换为可执行的 AI 视频生成提示词。


目标：

不是描述一个画面。

而是复制：

- 视觉逻辑
- 摄影语言
- 动作设计
- 情绪体验
- 制作方式

Seedance 2.0 约束：

- 每个生成段最长 15 秒。
- 超过 15 秒必须拆成多个 Segment；每个 Segment 单独提供提示词。
- 无论视频类型是变装/视觉变化还是 CG 产品广告，无论模式是完全复刻还是创作迁移，最终提示词都必须带逐镜头时间码。
- 每个 Segment 的镜头时间码必须覆盖完整段长，且画面、摄影机、转场、音效逐项对应；时间码必须先依据参考视频的真实镜头边界和节奏分析，再写入提示词。
- 默认无背景音乐，只提供按时间码排列的音效和环境声。


---

# Prompt Strategy

# 提示词生成策略


所有 Prompt 必须基于：

1. Director Intent

导演意图


2. Visual DNA

视觉DNA


3. Shot Design

镜头设计


4. Production Logic

制作逻辑

## 时间线整合规则

- AI 提示词必须严格按照参考视频的镜头时间线输出；该要求适用于产品视频和变装视频，不得只对变装视频执行。
- 每个 Segment 使用一个连续、可直接复制的提示词文本块。
- 在同一文本块内按实际时间码换行，例如 `00:00–[实际切点1]：...`、`[实际切点1]–[实际切点2]：...`；示例时间码不是固定分段建议。
- 时间码必须依据参考视频实际镜头边界和节奏曲线生成；不得默认使用 3 秒一段或其他均匀切分。若参考视频是快切、长停留或不规则节奏，提示词必须保留同样的不规则时长关系。
- 创作迁移保留参考视频的节奏骨架：快切段保持信息密度，长停留段保持展示时长，转场断点和结尾停留必须对应参考视频；迁移的是视觉方法和产品内容，不是重新平均分配时间。
- 每个时间码段必须把主体、动作、摄影机、构图、灯光、材质、转场和音效写在同一段文字中。
- 不要把摄影机、动作、灯光、材质分别输出成独立提示词栏目；这些栏目只用于内部组织分析，最终生成时必须合并。
- 最终交付禁止输出脱离时间线的整片笼统提示词。即使用户要求“只要关键词”，也必须把关键词写入对应的时间码段；无参考视频时只能输出明确标注为近似的时间线。



## 模式规则

提示词必须标明工作模式，并按模式执行：

- `REFERENCE_REPLICATION`：允许按用户要求复现参考视频的品牌、产品外观和表面元素；列出原样保留项与替换项。
- `CREATIVE_TRANSFER`：优先提取风格、镜头、情绪和方法，避免无目的复制表面资产。
- `CG_COMMERCIAL`：围绕产品英雄时刻、摄影机路径、材质、灯光、环境构建和视觉卖点组织提示词；工作模式仍根据用户选择使用 `REFERENCE_REPLICATION` 或 `CREATIVE_TRANSFER`。


---

# 1. Creative Direction

# 创意方向


## Concept

创意概念：


一句话描述视频核心：

>


---

## Emotional Goal

情绪目标：


希望观众感受到：

-


---

## Visual Style

视觉风格：

关键词：

-


---

# 2. Master Prompt

# 主提示词


用于直接输入 AI 视频模型。


结构：

[Subject]

[Environment]

[Action]

[Camera]

[Lighting]

[Material]

[Atmosphere]

[Style]

---

## Generated Prompt


```text

主体：

环境：

动作：

摄影机：

灯光：

材质：

氛围：

视觉风格：
```

## Timeline-integrated Production Prompt

最终生产提示词必须使用以下形式：

```text
00:00–00:03：主体与环境……动作与变化……摄影机与构图……灯光与材质……转场……SFX only, no background music；环境声/动作声/系统声……
00:03–00:06：承接上一时间段最后一帧……主体与环境……动作与变化……摄影机与构图……灯光与材质……转场……音效……
```

以上内容属于同一个连续提示词文本块，不得再拆成 Camera、Motion、Lighting、Material 等独立输出块。
3. Camera Prompt
摄影机提示词

> 内部构成项：将摄影机信息写入最终时间线提示词，不作为独立交付块输出。

描述导演摄影方案。

包含：

Shot Type

镜头类型：

例如：

cinematic wide shot
close-up
macro shot
hero shot
Lens

镜头感觉：

例如：

24mm wide lens
35mm cinematic lens
85mm portrait lens
Camera Movement

运动方式：

例如：

slow dolly in
orbit camera
tracking shot
crane movement
handheld movement
Camera Speed

速度：

slow motion
real-time
fast movement

输出：


Camera:

Lens:

Movement:

Speed:

4. Motion Prompt
动作提示词

> 内部构成项：将动作信息写入最终时间线提示词，不作为独立交付块输出。

用于控制：

人物、产品、环境运动。

包含：

Subject Motion

主体运动：

例如：

walking
rotating
transforming
floating
Motion Rhythm

运动节奏：

例如：

slow reveal
explosive transition
smooth cinematic movement
Transition Logic

转场逻辑：

例如：

match cut
camera occlusion
particle transformation
seamless morph

输出：


Movement:

Rhythm:

Transition:

5. Lighting Prompt
灯光提示词

> 内部构成项：将灯光信息写入最终时间线提示词，不作为独立交付块输出。

控制：

视觉质感。

包含：

Light Type

光源类型：

例如：

studio lighting
natural sunlight
neon lighting
Light Direction

方向：

例如：

backlight
side light
top light
Contrast

对比：

例如：

high contrast
soft cinematic
Color Temperature

色温：

例如：

warm golden
cool blue

输出：


Light Source:

Direction:

Contrast:

Color:

6. Material & Environment Prompt
材质与环境提示词

> 内部构成项：将材质和环境信息写入最终时间线提示词，不作为独立交付块输出。

尤其用于 CG Commercial。

包含：

Material

例如：

brushed metal
glossy surface
glass
carbon fiber
Environment

例如：

futuristic studio
industrial space
abstract world
Detail Level

例如：

ultra realistic
cinematic rendering
high detail

输出：


Material:

Environment:

Detail:

7. Style Control
风格控制
Cinematic Reference

描述：

电影感
广告感
摄影风格

例如：

premium automotive commercial style

cinematic product film

high-end fashion film

Quality Level

包含：

cinematic
realistic
professional
high production value
8. Negative Prompt
负面提示词

避免：

unwanted objects
incorrect anatomy
unstable motion
low quality
unrealistic lighting

示例：

avoid:

low resolution,
bad anatomy,
random movement,
distorted objects,
poor lightingFinal Prompt Output

最终输出：

Short Prompt

短版本：

适合快速生成。

Production Prompt

生产版本：

适合高质量生成。

Director Note

导演说明：

解释：

为什么这样设计。

Quality Check

检查：

□ Prompt 是否包含摄影设计

□ Prompt 是否包含运动逻辑

□ Prompt 是否包含光影

□ Prompt 是否来源于导演分析

□ Prompt 是否可执行

## Segment Prompts

每个 Segment 最长 15 秒，并且必须单独生成。每个 Segment 只输出一个按时间线组织的连续提示词文本块；时间码可以换行，但不得拆成多个提示词栏目。

### Segment 01

段长：

承接关系：

严格镜头时间线：

| 时间码 | 画面动作 | 摄影机/转场 | 音效 |
|---|---|---|---|
| 00:00–00:00 |  |  |  |

Seedance Prompt：

```text
00:00–00:00：只描述本段，严格遵守时间码，把画面动作、主体、摄影机、灯光、材质、转场和音效整合在同一连续文本块中，不加入超过本段范围的内容。
```

Audio Prompt：

```text
SFX only, no background music.
按时间码列出环境声、动作声、系统声和转场声。
```

### Segment 02

段长：

承接关系：

严格镜头时间线：

| 时间码 | 画面动作 | 摄影机/转场 | 音效 |
|---|---|---|---|
| 00:00–00:00 |  |  |  |

Seedance Prompt：

```text
00:00–00:00：只描述本段，严格遵守时间码，把画面动作、主体、摄影机、灯光、材质、转场和音效整合在同一连续文本块中，并说明如何承接上一段最后一帧。
```

Audio Prompt：

```text
SFX only, no background music.
按时间码列出本段音效，不引用未提供的音乐节拍。
```

Version

Version: 1.0

Purpose:

AI generation prompt structure for

Video Director Reverse Engineering Skill.
