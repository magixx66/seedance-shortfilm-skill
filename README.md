# Qisheng Seedance Director

这是一个面向 Seedance AI 短片与短剧的 Codex Skill。它把已确认的创意、故事或文学剧本转换为分镜、参考素材、人物一致性、运镜、灯光、声音和可执行生成方案。

## 适合做什么

- 单镜头或 15 秒 AI 电影提示词
- 60–90 秒多镜头 AI 短剧
- 历史题材的事实边界与戏剧化处理
- 人物、服装、场景和道具一致性
- 首尾帧衔接与分镜连续性
- 人物设定图、场景参考图、静态分镜图和首尾帧生成
- 参考图片、视频、音频的职责分配
- 失败镜头的原因诊断与最小修改

## 使用方式

可以直接说：

- 用我的 Seedance Skill，把雨夜车站重逢短片的第一幕做出来。
- 先为这个短片生成角色设定图、场景图和三个关键镜头首帧。
- 把这个镜头改成一个主动作和一个主运镜。
- 只参考 @视频1 的运镜，不参考人物和场景。
- 人物第二镜漂移了，帮我诊断并重写提示词。

也可以显式调用 $qisheng-seedance-director。

如果只需要构思故事或编写文学剧本，使用 `$qisheng-story-screenwriter`。完整流程为：

```text
qisheng-story-screenwriter
故事方案 → 文学剧本 → screenplay-to-director 交接包
  ↓
qisheng-seedance-director
分镜头脚本 → 镜头语言 → 视觉资产 → Seedance 提示词
```

导演 Skill 会保留交接包中锁定的剧情节点、对白、事实边界和连续性状态，只设计视觉表达。

## 核心规则

- 一个镜头，一个主动作，一个主运镜。
- 抽象情绪必须改写成可见的身体反应。
- 每个参考素材必须写清参考什么。
- 多镜头先建人物与资产清单，再写提示词。
- 静态分镜图只表现一个可以被拍成照片的瞬间。
- 用 Continuity Lock 固定身份与世界，用 Shot Delta 描述本镜变化。
- 平台规格会变化，真正生成前必须核对当前限制。

仓库可以命名为 seedance-shortfilm-skill，安装目录应保持为 qisheng-seedance-director，以匹配 Skill 名称。

## License

本项目采用 MIT License。SOURCES.md 所列参考仓库及其原始内容仍分别遵循各自的许可证或版权声明。
