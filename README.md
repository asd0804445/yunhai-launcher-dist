# 雲海紀元啟動器 — 更新發布

本 repo 供「雲海紀元」啟動器自動更新使用。

- `update.json`：更新資訊清單。啟動器會讀取此檔比對版本。
- Releases：存放各版本 exe。

## 發布新版流程
1. 用新原始碼建置出 exe，取得其 SHA-256。
2. 到 Releases 建立新 tag（如 `v1.1`），上傳 exe（檔名建議 ASCII，如 `YunHaiLauncher.exe`）。
3. 修改本檔 `update.json`：`versionCode` +1、更新 `versionName`、`url`（指向新 Release 的 exe）、`sha256`、`notice`。
4. 提交推送。玩家下次開啟啟動器即自動更新。

> `versionCode` 必須與原始碼 `ModBase.vb` 的 `VersionCode` 一致。
