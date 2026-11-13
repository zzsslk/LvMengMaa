<!-- markdownlint-disable MD033 MD041 -->
<p align="center">
  <img alt="LOGO" src="resource/logo.png" width="128" />
</p>

<p align="center">
  <img alt="framework" src="https://img.shields.io/badge/MaaFramework-LGPL--3.0-blue">
  <img alt="platform" src="https://img.shields.io/badge/platform-Windows-blueviolet">
  <img alt="license" src="https://img.shields.io/badge/license-AGPL--3.0-green">
</p>

<div align="center">

# 绿梦：时空之声 MAA

基于图像识别技术的《绿梦：时空之声》自动化工具（MuMu 模拟器平台）

</div>

## 项目说明

本项目是《绿梦：时空之声》（3D 科幻横版 ACT + 卡牌养成二游，开发商「竹子游戏」）的自动化辅助工具，基于 [MaaFramework](https://github.com/MaaXYZ/MaaFramework) 图像识别框架构建，运行于 MuMu 12 模拟器。

## 已实现功能

| 功能 | 说明 |
|------|------|
| 战斗流程 | 主菜单→蚀务日常→副本→构战回廊→受蚀者·异变体-I→开始挑战→出战，战斗三键连点直至结算「挑战成功」 |
| 蚀务之礼签到 | 活动限时签到，领取「高能频带」 |
| 值勤作战补给 | 每日登录自动签到（累计登录奖励） |
| 奇遇臻选赏奖券 | 「今日获取奖券」任务领取 |

## 用了什么（技术栈）

| 组件 | 用途 | 协议 |
|------|------|------|
| [MaaFramework](https://github.com/MaaXYZ/MaaFramework) | 图像识别自动化框架（核心） | LGPL-3.0 |
| [MFAAvalonia](https://github.com/MaaXYZ/MaaFramework) | 官方 Avalonia 桌面 UI（界面） | LGPL-3.0 |
| PaddleOCR（ppocr_v6） | 文字识别（OCR 模型） | Apache-2.0 |
| MuMu 12 模拟器 ADB | 设备连接与截图输入 | — |
| DeepSeek Harness（DSH） | 智能体全程制作 | — |

- 界面参照 [MaaAutoNaruto](https://github.com/duorua/narutomobile)（火影忍者 MAA）的 MFAAvalonia 样式。
- 项目模板来自 [MaaPracticeBoilerplate](https://github.com/MaaXYZ/MaaPracticeBoilerplate)。

## 环境要求

- Windows 10/11
- [MuMu 12 模拟器](https://mumu.163.com/)（分辨率 16:9 横屏，1600×900）
- 游戏《绿梦：时空之声》已安装并能正常进入
- VC++ 运行库（v14.x）

## 快速开始

1. 从 [Release 页面](../../releases) 下载最新版本解压
2. 启动 MuMu 12 模拟器，确保分辨率 16:9 横屏
3. 运行 `MFAAvalonia.exe`
4. 在「连接模拟器」选择 adb 地址（默认 `127.0.0.1:16416`）
5. 勾选任务，点击启动

## 目录结构

```
├── MFAAvalonia.exe          # 主程序（官方 UI）
├── interface.json           # 项目接口定义（PI v2）
├── resource/
│   ├── logo.ico / logo.png  # 项目图标
│   └── announcement/        # 公告（简介/用户协议）
├── assets/resource/
│   ├── base/
│   │   ├── image/           # 模板图
│   │   ├── model/ocr/       # OCR 模型（det.onnx/rec.onnx/keys.txt）
│   │   └── pipeline/        # 任务流水线 JSON
│   └── ...
└── scripts/                 # 开发用 Python 脚本（daily.py/full_flow.py 等）
```

## 免责声明

- 本软件仅供学习研究 MaaFramework 图像识别技术使用。
- 使用本软件可能违反游戏服务条款，**存在账号封禁风险**，后果由使用者自行承担。
- 本项目不修改游戏数据、不绕过反作弊机制，仅模拟人工点击。

## 开源协议

本项目遵循 **AGPL-3.0** 协议开源，详见 [LICENSE](LICENSE)。

## 制作声明

**本项目全程由 DeepSeek Harness（DSH）智能体「大肥鱼」制作。** 🐟
