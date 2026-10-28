<div align="center">

# TrainingGround

**一个 Unity 3D 技术展厅**

仿《王者荣耀》训练营：一个人、一片空地、敌人走过来，旁边一排开关。<br>
不追求做成完整的游戏，目标是把 Unity 客户端常用的技术各做一个能看、能讲的演示。

![Unity](https://img.shields.io/badge/Unity-6000.3.26f1%20LTS-black?logo=unity)
![URP](https://img.shields.io/badge/渲染管线-URP-blue)
![Version](https://img.shields.io/github/v/tag/HuA4xgkUzy/TrainingGround?label=版本&sort=semver)
![Status](https://img.shields.io/badge/状态-施工中-orange)

</div>

---

## 目录

- [规划内容](#规划内容)
- [进度](#进度)
- [快速开始](#快速开始)
- [项目结构](#项目结构)
- [开发规范](#开发规范)
- [素材来源](#素材来源)

## 规划内容

| 场景 | 展示什么 |
|---|---|
| ⚔️ 战斗场景（C# 版 → Lua 版 / HybridCLR 版） | Animator 状态机、混合树、动画帧事件、受击与打击感、对象池、NavMesh 寻路；半透明小窗实时显示正在执行的代码；热更新前后对比 |
| 🏰 UI 大厅 | 红点、事件系统、循环列表背包、UI 管理器、配置表、签到、存档、图集与 DrawCall 对比、多分辨率适配 |
| 🔥 热更新 | HybridCLR（C# 热更）+ xLua（Lua 热更）+ YooAsset 资源更新 |

## 进度

- [x] 建项目（Unity 6.3 LTS + URP）
- [ ] 主城 UI 第一阶段：资源栏、入口按钮和红点、面板开关
- [ ] 主城 UI：背包、邮件、任务、商店
- [ ] 战斗场景（C#）
- [ ] 战斗场景：Lua 版 / HybridCLR 版 + 代码执行小窗
- [ ] 资源热更新

每完成一个阶段打一个版本号，见 [版本列表](https://github.com/HuA4xgkUzy/TrainingGround/tags)。

## 快速开始

需要：macOS、Unity **6000.3.26f1**（请用这个版本，别让 Hub 升级）、[Git LFS](https://git-lfs.com)。

```bash
brew install git-lfs && git lfs install
git clone https://github.com/HuA4xgkUzy/TrainingGround.git
```

在 Unity Hub 里「添加」这个文件夹，用 6000.3.26f1 打开。第一次打开要重新生成 `Library/`，等几分钟。打开 `Assets/Scenes/` 里的场景，按 ▶ 运行。

> 图片、模型、字体、音频走 Git LFS。没装 LFS 就克隆的话，这些文件只是几行文字的「指针」，Unity 里会显示丢失。

AI 接手或换电脑时的完整说明见 [AGENTS.md](AGENTS.md)。

## 项目结构

```
Assets/
  Scenes/      场景
  Scripts/     代码
  UI/          界面预制体
  Settings/    URP 渲染设置
docs/
  提交规范.md  提交信息怎么写
```

## 开发规范

- 提交信息按 [提交规范](docs/提交规范.md)：`类型(范围): 一句话`，写清楚改了什么、为什么。
- 版本号用 `v大.中.小`：完成一个阶段升中版本，修小问题升小版本。
- Unity 场景、预制体冲突时，Git 交给 Unity 自带的 UnityYAMLMerge 合并（配置见 [AGENTS.md](AGENTS.md)）。

## 素材来源

- 3D 模型与动画：[KayKit](https://kaylousberg.itch.io/)（CC0）
