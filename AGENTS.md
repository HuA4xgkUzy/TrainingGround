# AGENTS.md · TrainingGround

> 给 AI 的接手说明（[agents.md](https://agents.md) 格式）。人看的介绍在 [README.md](README.md)，提交格式在 [docs/提交规范.md](docs/提交规范.md)。
> 用户的总规矩在 iCloud「AI交接包」的 `AGENTS.md`，进度和教学方式在交接包 `项目/游戏作品集.md`。**这是公开仓库**，任何东西提交前都想一下能不能给全世界看。

## 最重要的一条：用户在亲手学

用户在借这个项目重学 Unity。**不要替他一口气做完**：一步步讲，每步让他自己在 Unity 里操作，再回报看到了什么；每步讲「为什么」；Windows 教程换成 Mac 按键讲。学到的要点简要存进 Obsidian。进度看交接包 `项目/游戏作品集.md`（UGUI 第几课）。

## 在新电脑上从零部署

```bash
brew install git-lfs && git lfs install          # 图片、模型、字体、音频走 Git LFS，没装的话拉下来只是指针文件
git clone https://github.com/HuA4xgkUzy/TrainingGround.git ~/Projects/TrainingGround
cd ~/Projects/TrainingGround
# 冲突时让 Git 用 Unity 自带的合并工具处理场景、预制体（每台电脑配一次，不进仓库）
git config merge.unityyamlmerge.name "Unity SmartMerge"
git config merge.unityyamlmerge.driver "'/Applications/Unity/Hub/Editor/6000.3.26f1/Unity.app/Contents/Helpers/UnityYAMLMerge' merge -p %O %B %A %A"
```

- Unity **必须是 6000.3.26f1**（6.3 LTS）。别让 Hub 用 6.6 打开，会升级而且退不回去。
- 命令行打开：`open -a "/Applications/Unity/Hub/Editor/6000.3.26f1/Unity.app" --args -projectPath ~/Projects/TrainingGround`
- 第一次打开会重新生成 `Library/`，要等几分钟，这是正常的。
- 代码编辑器用 Rider。用户提交用 GitHub Desktop，它自带 LFS。

## 怎么验证跑通

Unity 打开没有红色报错，`Assets/Scenes/` 里的场景按 ▶ 能运行。

## 规矩

- 编辑器开着的时候，不要用命令行批处理这个项目。
- 用户说「先别提交」的文件不要碰（现在是主城 UI，见 AI交接包 `工具/体检暂缓.txt`）。
- 素材只用能公开的（KayKit 是 CC0）。Asset Store 的素材不能进这个公开仓库。
- 提交按 `docs/提交规范.md` 写。

## 版本号

Git 标签 `v大.中.小`，规则见交接包 `AGENTS.md` 第 2 节。每完成一个阶段升中版本（比如 v0.2.0 = 主城 UI 第一阶段）。游戏项目，用户说「这版好」时发 GitHub Release，附说明和能玩的包。
