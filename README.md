# chefeibao-update

车险报价单 App 的更新信息仓库。本仓库**仅存放**：

- `version.json`：最新版本号与下载渠道
- 各版本 Release 的 APK 二进制（作为 GitHub 备用下载渠道）

主代码仓库保持私有。

## 字段说明

```json
{
  "version": "1.0.0",
  "versionCode": 1,
  "primary": {
    "url": "https://wwaqd.lanzoum.com/...",  // 蓝奏云主链接
    "password": "xxxx"                         // 蓝奏云分享密码
  },
  "backup": {
    "url": "https://github.com/zhyao111/chefeibao-update/releases/download/v1.0.0/app-debug.apk"
  },
  "note": "更新说明"
}
```

App 通过 jsdelivr CDN 拉取本仓库 `version.json`，国内可直连。

## 发布新版本流程

1. 在私有主仓库打 APK
2. 上传 APK 到蓝奏云 → 拿链接/密码
3. 上传 APK 到本仓库的 Release → 拿资产直链
4. 修改本仓库 `version.json` → push main 分支