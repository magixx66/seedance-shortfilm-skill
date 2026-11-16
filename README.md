# Qisheng Seedance Director

这是一个面向 Seedance AI 短片与短剧的 Agent Skill（兼容 Codex、Antigravity、Claude Code 等支持 Agent Skills 的客户端）。它把已确认的创意、故事或文学剧本转换为分镜、参考素材、连续性控制、可复制生成提示词、后期交接单与失败修复方案。

## 适合做什么

- 单镜头（4–10 秒）或连续长镜头（15 秒时间轴）AI 电影提示词
- 60–90 秒多镜头、多场次 AI 短剧（支持 `16:9` 横屏与 `9:16` 竖屏安全区）
- 历史/年代题材的事实边界与反穿帮检查
- `Project Bible` → `Scene Lock` → `Shot Delta` 三层连续性控制
- 人物设定图、场景参考图、静态分镜图和首尾帧生成
- 逻辑资产 ID 与单镜平台槽位（`@图片1` / `@视频1`）分离映射
- 对白口型时长控制、声音四层设计与后期剪辑交接（Handles / J-L cut / 字幕）
- 失败镜头的原因诊断与最小单变量修改

## 使用方式

可以直接说：

- 用我的 Seedance Skill，把雨夜车站重逢短片的第一幕做出来（9:16 竖屏）。
- 先为这个短片生成角色设定图、场景图和三个关键镜头首帧。
- 把这个镜头改成一个主动作和一个主运镜，并给我纯中文可复制提示词。
- 只参考 @视频1 的运镜，不参考人物和场景。
- 人物第二镜漂移了，帮我诊断并给出最小单变量改写。

也可以显式调用 `$qisheng-seedance-director`。

如果只需要构思故事或编写文学剧本，使用 `$qisheng-story-screenwriter`。完整流程为：

```text
qisheng-story-screenwriter
故事方案 → 文学剧本 → screenplay-to-director 交接包
  ↓
qisheng-seedance-director
三层连续性 → 分镜脚本 (S01-01) → 视觉资产 → Shot Card + Copy-ready Prompt → 后期交接单
```

导演 Skill 会保留交接包中锁定的剧情节点、对白、事实边界和连续性状态，只设计视觉表达。

## 核心规则

- 一个镜头，一个主动作，一个主运镜；每镜首尾各留约 `0.5s` 剪辑余量（Handles）。
- **Shot Card 与 Copy-ready Prompt 分离**：控制卡放调度与接力信息，纯提示词干净直接复制进生成框。
- **逻辑资产 ID 与平台槽位分离**：先定 `CHAR_01` / `LOC_01`，每镜再绑定 `@图片1` / `@视频1`。
- **三层连续性**：`Project Bible`（全片）→ `Scene Lock`（单场）→ `Shot Delta`（单镜）。
- 抽象情绪必须改写成可见的身体反应；静态分镜图只表现一个可拍瞬间。
- 平台规格与引用语法会变化，真正生成前必须填写预检核对记录卡。

仓库可以命名为 `seedance-shortfilm-skill`，安装目录应保持为 `qisheng-seedance-director`，以匹配 Skill 名称。

## 目录结构

| 路径 | 作用 |
|---|---|
| `SKILL.md` | 核心原则、中英触发边界、路由表与 8 步导演流程 |
| `assets/continuity-lock-template.md` | 三层连续性模板（Project Bible / Scene Lock / Shot Delta）与状态接力表 |
| `assets/prompt-templates.md` | 槽位映射表、Shot Card + Copy-ready Prompt 分离模板与双镜完整范例 |
| `references/` | 编剧交接、分镜与 9:16 语法、运镜、光色、声音口型、预制作、短剧后期交接、系统预检、排错与质检 |
| `agents/openai.yaml` | Codex / OpenAI 界面元数据与默认调用配置 |
| `SOURCES.md` | 方法来源与许可证处理说明 |

## License

本项目采用 MIT License。SOURCES.md 所列参考仓库及其原始内容仍分别遵循各自的许可证或版权声明。
