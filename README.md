# LEXI｜易混词辨析

英语易混词辨析与智能记忆系统。网页版直接打开 `index.html` 或访问 https://zeng-maker-ai.github.io/yihun-vocab/

- 词库：373 组 / 828 词（人教、译林课标层级 + 四六级），IPA 全覆盖
- 功能：查词、两词智能对比、发音对比（TTS + 英美音）、我的收藏与备注、五种辨析训练、SM-2 间隔复习、PWA 离线可用

## Android APK（GitHub Actions 自动构建）

推送 `main` 分支后自动构建，APK 发布在 [Releases](../../releases/tag/v2.0)：

1. 本仓库根目录 `www/` 为 WebView 打包用网页资源
2. `android/` 为 Capacitor 生成的安卓工程（含签名配置，证书随仓库提交，仅限个人使用）
3. `.github/workflows/android.yml` 在每次 push 后：`npm ci` → `gradlew assembleDebug assembleRelease` → 上传 Artifact 并更新 Release v2.0

本地维护：改 `www/index.html`（或上游 `lexi/dist`）→ push → Actions 自动出新 APK。

## 网页版数据来源

词库整理自人教/译林课标词表与四六级词表；例句为精选教学参考；词典补充用 Free Dictionary API（联网时自动缓存）。复习算法为 SM-2 间隔重复。
