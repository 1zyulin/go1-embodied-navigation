# 四周核心论文与官方仓库

> 日期：2026-10-28。开源仓库存在不代表训练/仿真/权重全部完整可复现；运行前需再次检查版本和许可证。

| 周次 | 论文 / 方向 | 正式发表 | 论文 | 作者仓库 |
|---|---|---|---|---|
| W1-A | **NaVILA: Legged Robot Vision-Language-Action Model for Navigation**：四足 VLA/分层导航 | RSS 2025 | [主页/论文](https://navila-bot.github.io/) | [AnjieCheng/NaVILA](https://github.com/AnjieCheng/NaVILA) |
| W1-B | **VLFM: Vision-Language Frontier Maps for Zero-Shot Semantic Navigation**：前沿与目标地图 | ICRA 2024 | [arXiv](https://arxiv.org/abs/2312.03275) | [rai-opensource/vlfm](https://github.com/rai-opensource/vlfm) |
| W2-A | **ApexNav: An Adaptive Exploration Strategy for Zero-Shot Object Navigation With Target-Centric Semantic Fusion**：目标探索 | RA-L 2025 / ICRA 2026 | [DOI](https://doi.org/10.1109/LRA.2025.3606388) | [Robotics-STAR-Lab/ApexNav](https://github.com/Robotics-STAR-Lab/ApexNav) |
| W2-B | **VLN-Game: Vision-Language Equilibrium Search for Zero-Shot Semantic Navigation**：描述式目标搜索 | T-RO 2026 | [DOI](https://doi.org/10.1109/TRO.2026.3677047) | [ybgdgh/VLN-Game](https://github.com/ybgdgh/VLN-Game) |
| W3-A | **ComposableNav: Instruction-Following Navigation in Dynamic Environments via Composable Diffusion**：动态避障 | CoRL 2025 | [项目/论文](https://amrl.cs.utexas.edu/ComposableNav/) | [ut-amrl/ComposableNav](https://github.com/ut-amrl/ComposableNav) |
| W3-B | **ByteTrack: Multi-Object Tracking by Associating Every Detection Box**：行人跟踪 | ECCV 2022 | [arXiv](https://arxiv.org/abs/2110.06864) | [ifzhang/ByteTrack](https://github.com/ifzhang/ByteTrack) |
| W4-A | **VLMaps: Building Visual-Language Maps for Robot Navigation**：地点与空间语义 | ICRA 2023 | [arXiv](https://arxiv.org/abs/2210.05714) | [vlmaps/vlmaps](https://github.com/vlmaps/vlmaps) |
| W4-B | **Grounding DINO: Marrying DINO with Grounded Pre-Training for Open-Set Object Detection**：开放词汇检测 | ECCV 2024 | [arXiv](https://arxiv.org/abs/2303.05499) | [IDEA-Research/GroundingDINO](https://github.com/IDEA-Research/GroundingDINO) |

## 选型备注

- **ApexNav** 是优先动手的 ObjectNav 基线，有官方 Habitat 评测与真实环境示例。主分支测试环境是 Ubuntu 20.04、ROS Noetic 和较旧 PyTorch；另有 ROS2 Jazzy 分支，仍需核对实际 Go1 适配。
- **VLFM** 可作为另一种语义前沿地图基线，但旧环境依赖较重。
- **ComposableNav** 有数据生成、监督预训练、RL 微调和 notebook demo；先尝试可运行的最小 demo，不以四周从头训练全部模型为目标。
- **NaVILA** 用于理解高层语言指令与下层运动的分离；不代表直接兼容 Go1。
- **Grounding DINO** 负责识别人/物体候选，不能代替测距、目标身份确认、行人动态避障。
- **VLN-Game、VLMaps** 帮助设计语言描述和地点搜索，不是独立的安全控制器。

补充工程参考：[Nav2 Collision Monitor](https://docs.nav2.org/jazzy/configuration_and_development/configuration_guide/core_servers/collision_monitor/)。传感器驱动的减速/停车机制仍需完整安全评估。

> 将作者原有许可证、README、论文引用与实际执行的 commit 号记入实验记录。不要上传受限 HM3D 数据或未经许可的模型权重。
