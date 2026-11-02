# Shot Timeline Template

# 镜头时间线拆解模板


## Purpose

用于对参考视频进行镜头级逆向工程分析。

每一个 Shot 代表一个具有独立视觉目的的导演决策单元。


分析目标：

不是记录：

“这个镜头有什么”


而是理解：

“这个镜头为什么存在，以及如何实现。”


---

# Shot Information

# 镜头基础信息


工作模式：

- REFERENCE_REPLICATION（完全模仿）
- CREATIVE_TRANSFER（创作迁移）

视频类型：CG_COMMERCIAL（CG 产品视频，可与上述任一工作模式组合）


## Shot ID

镜头编号：

Example:

SHOT_001


---

## Timecode

时间范围：

开始：

结束：


持续时间：

所属分段：

分段总时长：

节奏依据：

记录该镜头为何在此处切换，以及它与前后镜头的时长关系。不得默认按固定时长均分；时间码应来自实际镜头边界或有依据的估计。


---

## Shot Type

镜头类型：


选择：

- Establishing Shot
  建立镜头


- Hero Shot
  主角/产品英雄镜头


- Detail Shot
  细节展示镜头


- Action Shot
  动作镜头


- Transition Shot
  转场镜头


- Reveal Shot
  揭示镜头


- Emotional Shot
  情绪镜头


---

# Layer 1

# Visual Observation

# 视觉观察


## Subject

主体：

记录画面主要对象。


例如：

- 人物
- 产品
- 环境
- 道具


---

## Action

动作：

描述实际发生的动作。


禁止解释。


Example:

正确：

“人物抬手遮挡镜头。”


错误：

“人物表现出神秘感。”


---

## Environment

环境：

记录：

- 空间
- 背景
- 场景元素


---

## Camera Observation

摄影机观察：


记录：

- 景别
- 角度
- 运动
- 镜头方向


---

## Audio Observation

声音观察：

记录：

- 音乐变化
- 音效
- 人声
- 节奏节点

音效时间码：

背景音乐：默认无（只有用户明确要求时才添加）



---

# Layer 2

# Visual Language

# 视觉语言分析


## Camera Language

摄影语言：

分析：

- 镜头选择
- 焦段感觉
- 运镜方式
- 摄影机速度


---

## Lighting Language

灯光语言：

分析：

- 光源方向
- 明暗关系
- 对比度
- 色温


---

## Composition Language

构图语言：

分析：

- 主体位置
- 空间关系
- 视觉焦点
- 留白


---

## Motion Language

运动语言：

分析：

- 动作节奏
- 速度变化
- 动态冲击


---

## Color Language

色彩语言：

分析：

- 主色
- 辅助色
- 色彩情绪


---

# Layer 3

# Director Intent

# 导演意图


## Shot Purpose

镜头目的：


这个镜头存在的原因：

例如：

- 建立世界
- 制造期待
- 展示细节
- 情绪升级
- 品牌强化


---

## Observation

观察事实：

基于画面的客观信息。


---

## Interpretation

导演推断：


为什么导演这样设计？


---

## Audience Effect

观众效果：

希望观众产生：

- 注意
- 好奇
- 兴奋
- 信任
- 惊喜
- 情绪共鸣


---

## Confidence

可信度：

0-1


---

## Evidence

证据：

包含：

- 时间码
- 关键帧
- 可观察元素


---

# Layer 4

# Production Logic

# 制作逻辑


## Production Type

制作类型：

选择：

- Real Shooting
  真人拍摄


- CG Production
  CG制作


- CG Commercial
  CG 产品视频制作



---

## Creation Method

实现方式推测：


真人：

- 演员动作
- 摄影设备
- 剪辑方式
- 后期效果


CG：

- 建模
- 材质
- 动画
- 灯光
- 渲染
- 特效


---

## Required Assets

所需资产：


角色：

产品：

环境：

模型：

材质：

特效：


---

## Technical Difficulty

技术难度：

等级：

- Low
- Medium
- High
- Extreme


原因：

## Audio Production

音效设计：

音效时间线：

背景音乐：默认无。若用户未明确要求，必须写 `SFX only, no background music`。


---

# Layer 5

# Creative Transfer

# 创作迁移


## Core Principle

核心创作原则：


这个镜头真正值得学习的是：


>


---

## Adaptation Opportunity

应用机会：


可以应用于：


- 产品广告
- 品牌视频
- 短视频
- AI视频生成



---

## Preserve

保留：

必须保持的创意元素：


-


---

## Replace

替换：

可以变化的元素：


-


---

# AI Prompt Translation

# AI提示词转换


## Scene Prompt

场景提示词：

```text
摄影机提示词：
运动提示词：
灯光提示词：
材质提示词：
一句话导演总结：
检查：

□ 是否描述事实而非猜测

□ 是否解释导演意图

□ 是否提供证据

□ 是否分析制作方式

□ 是否具有迁移价值Version
```

Version: 1.0

Purpose:

Core shot-level structure for

Video Director Reverse Engineering Skill.
