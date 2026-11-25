# BOXLOG 公开发布仓库

这里只放 BOXLOG 的可下载发布物，源码在私有仓库 `bfyoy-zzl/BOXLOG`。

## 每个 Release 的资产

- `BOXLOG-windows-portable.zip`：Windows 便携版，解压即用，也是电脑端自更新使用的包。
- `BOXLOGSetup.exe`：Windows 安装器。
- `manifest.json`：电脑端更新清单，包含版本、build 号、每个文件的 SHA-256 和大小。
- `BOXLOG-<version>.apk`：安卓安装包。

`manifest.json` 必须放在 Release 资产里；电脑端从 `releases/latest/download/manifest.json` 读取。Release 不要设为草稿或预发布，否则 `latest` 找不到。

## 签名

安卓正式包必须使用固定的 release keystore 签名；keystore 和密码不进入任何仓库。
