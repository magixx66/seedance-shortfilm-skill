# Sources and adaptation notes

本 Skill 对以下公开资料进行了方法层面的筛选、交叉核对与重新组织。正文为重新编写，没有整段搬运原文。

## 1. JHBOY-ha/seedance-2-prompt-guide

- 地址：https://github.com/JHBOY-ha/seedance-2-prompt-guide
- 吸收内容：结构化提示词、时间轴、参考素材职责、运镜选择、检查与排错。
- 处理方式：压缩为稳定工作流；没有把容易变化的平台参数写成永久事实。
- 仓库检查时未见明确许可证文件，使用时应以原仓库最新声明为准。

## 2. seedanceprompts/seedance-prompts

- 地址：https://github.com/seedanceprompts/seedance-prompts
- 吸收内容：作为 Seedance 相关工具、教程和资源的发现入口。
- 处理方式：不把资源索引本身当作权威产品规格。
- 仓库声明为 CC BY 4.0；再分发其原文时应保留相应署名。

## 3. issastash/AI_Complete_Prompting_Guides

- 地址：https://github.com/issastash/AI_Complete_Prompting_Guides
- 吸收内容：从“描述者”转为“导演”、镜头脚本、引用标签、连续性、延长镜头与逐变量排错。
- 处理方式：将长篇教程改造成按任务读取的参考文件。
- 仓库检查时未见明确许可证文件，使用时应以原仓库最新声明为准。

## 4. babakarto/PromptiusMaximus

- 地址：https://github.com/babakarto/PromptiusMaximus
- 吸收内容：主动作/主运镜约束、声音分层、灯光逻辑、长视频分段、风格锁定和失败诊断。
- 明确排除：绕过审核、人脸检测规避、安全过滤规避等内容。
- 仓库检查时未见明确许可证文件，使用时应以原仓库最新声明为准。

## 5. inference-sh/skills

- 地址：https://github.com/inference-sh/skills
- 吸收内容：180 度轴线、视线匹配、动作匹配、屏幕方向和分镜标注字段。
- 处理方式：重写为模型无关的分镜空间语法，不依赖其专属命令行工具。
- 仓库检查时未见明确许可证文件，没有复制原文或代码。

## 6. NPR9/cinematic-prompt-skills

- 地址：https://github.com/NPR9/cinematic-prompt-skills
- 吸收内容：设定板到分镜再到逐镜视频 Prompt 的分阶段流程、服装锁定和静态分镜瞬间规则。
- 处理方式：改写为可选图片预制作流程，不强制固定网格或固定面板数量。
- 仓库声明为 MIT License。

## 7. NBchitu/cinematic-storyboard-generator

- 地址：https://github.com/NBchitu/cinematic-storyboard-generator
- 吸收内容：视觉风格圣经、连续性锚点、转场意图、分镜图生成和拆分思路。
- 处理方式：保留可复用的制作逻辑，不强制用户每次选择导演风格，也不复制脚本或模板原文。
- 仓库检查时未见明确许可证文件，没有复制原文或代码。

## 8. ningbainb/cinematic-visual-generation-skill

- 地址：https://github.com/ningbainb/cinematic-visual-generation-skill
- 吸收内容：Continuity Lock、Shot Delta、写实画面的生活细节和逐变量修正。
- 处理方式：扩展为图片和视频都能使用的连续性模板。
- 仓库声明为 MIT License。

## 9. lrvaka/claude-skills

- 地址：https://github.com/lrvaka/claude-skills
- 吸收内容：图片编辑中分开描述修改项与保留项、多图职责和单变量迭代。
- 处理方式：与内置 imagegen 的安全工作流结合，未采用第三方 API 运行方式。
- 仓库声明为 MIT License。

## 10. gainubi/storyboard-video-skill

- 地址：https://github.com/gainubi/storyboard-video-skill
- 吸收内容：故事动力、视觉母题、分镜节奏和每格承担不同叙事功能。
- 处理方式：融合进分镜语法与质量检查，没有复制提示词正文。
- 仓库检查时未见明确许可证文件，没有复制原文或代码。

## 适用原则

不同资料对分辨率、时长、输入数量、真人参考与功能支持存在冲突。这些属于会变化的产品信息。实际生成前应核对目标模型和官方界面的当前能力；本 Skill 只把相对稳定的导演、分镜与提示词方法固化下来。
