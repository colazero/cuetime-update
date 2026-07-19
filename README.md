# CueTime 更新仓库

桌面端自动更新源。

## 结构
- `desktop/windows/latest.json` — Tauri updater 检查此文件
- `desktop/windows/*.exe` — NSIS 安装包
- `desktop/windows/*.sig` — 签名文件

## 发版流程
1. 主项目 `cargo tauri build`
2. 把 `.exe` + `.sig` 拷到 `desktop/windows/`
3. 更新 `latest.json`
4. 创建 GitHub Release 上传文件
5. `git push`
