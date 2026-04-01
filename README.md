# 无障碍授权管理器 (Accessibility Timer Manager)

## 🔥 更新日志 v4.0 - 录屏防护版

- ✅ **新增录屏防护监控** - 📹 检测到录屏 + 无障碍时自动关闭（防诈骗）
- ✅ **新增夜间锁屏防护** - 🌙 夜间锁屏时自动关闭所有无障碍
- ✅ **新增早晨自动恢复** - ☀️ 早晨解锁时恢复可信应用
- ✅ **新增安全设置界面** - 可配置所有防护选项
- ✅ 代码混淆保护（防止反编译）
- ✅ GitHub Actions 自动编译

## 🛡️ 防诈骗场景

本应用特别适合防止诈骗软件滥用无障碍权限：

- ✅ **录屏防护** - 📹 检测到录屏 + 无障碍时自动关闭（最新！）
- ✅ 即使被骗开启无障碍，也会自动关闭
- ✅ 夜间自动关闭，防止夜间恶意操作
- ✅ 集中管理，一眼看到所有启用的应用
- ✅ 一键关闭，紧急情况下快速防护

**详细防护指南：**
- 📹 录屏防护说明：[SCREEN_RECORD_PROTECTION.md](SCREEN_RECORD_PROTECTION.md)
- 🛡️ 综合安全指南：[SECURITY_GUIDE.md](SECURITY_GUIDE.md)

## 功能说明

本应用用于管理 Android 无障碍服务的授权时间，支持：

1. **多应用管理** - 管理任何应用的无障碍授权时间
2. **定时关闭** - 为每个应用独立设置关闭时间
3. **夜间防护** - 🌙 夜间锁屏时自动关闭所有无障碍（防诈骗）
4. **早晨恢复** - ☀️ 早晨解锁时恢复可信应用
5. **开机重置** - 设备重启后自动关闭无障碍授权
6. **一键关闭** - 紧急情况下快速关闭所有
7. **代码混淆** - 防止被反编译和修改
8. **自动编译** - GitHub Actions 云端自动构建 APK

## 系统要求

- Android 7.0+
- 需要授予 `WRITE_SECURE_SETTINGS` 权限（通过 ADB）

## 📥 快速开始（无需电脑！）

### 方法 1: GitHub Actions 自动编译（推荐）

1. 注册 GitHub 账号：https://github.com/signup
2. 创建新仓库
3. 上传本项目所有文件
4. GitHub Actions 会自动编译
5. 在 Actions 页面下载 APK

**详细教程：** 查看 [GITHUB_GUIDE.md](GITHUB_GUIDE.md) 或 [QUICK_START.md](QUICK_START.md)

### 方法 2: 本地编译（需要电脑）

```bash
cd accessibility-timer-app
./gradlew assembleDebug
adb install app/build/outputs/apk/debug/app-debug.apk
```

## 🔐 授权步骤

```bash
# 授予写入安全设置的权限
adb shell pm grant com.accessibility.timer android.permission.WRITE_SECURE_SETTINGS

# 授予开机启动权限
adb shell pm grant com.accessibility.timer android.permission.RECEIVE_BOOT_COMPLETED
```

## 📱 使用方法

### 基础使用

1. 打开应用，查看已启用无障碍的应用列表
2. 点击任意应用，设置定时关闭时间
3. 倒计时结束后，该应用的无障碍权限自动关闭

### 安全配置（推荐）

1. 打开应用 → 点击 **安全设置**
2. 启用以下选项：
   - ✅ 开机自动关闭
   - ✅ 夜间锁屏防护（设置时间段：22:00 - 07:00）
   - ✅ 早晨自动恢复（可选）
3. 保存设置

### 紧急防护

- 发现可疑应用 → 点击 **关闭所有** 按钮
- 夜间锁屏 → 自动关闭所有无障碍
- 设备重启 → 自动清除所有授权

## ⚠️ 注意事项

- 本应用需要系统级权限，仅适用于已 Root 或可通过 ADB 授权的设备
- 无法阻止用户首次开启无障碍（需用户自行防范）
- 最佳防护是：不贪、不信、不转账

## 📚 文档

| 文档 | 说明 |
|------|------|
| [SECURITY_GUIDE.md](SECURITY_GUIDE.md) | 🛡️ 防诈骗安全防护指南 |
| [QUICK_START.md](QUICK_START.md) | 📱 5 分钟快速上手教程 |
| [GITHUB_GUIDE.md](GITHUB_GUIDE.md) | 📦 GitHub 注册与使用教程 |
| [INSTALL_GUIDE.md](INSTALL_GUIDE.md) | 🔧 详细安装配置指南 |
| [FEATURES.md](FEATURES.md) | 📋 完整功能说明 |

## 技术架构

- **语言**: Kotlin
- **最低 API**: 24 (Android 7.0)
- **目标 API**: 34 (Android 14)
- **架构**: MVVM

## 许可证

MIT License

---

**最好的防护是防范意识，本应用只是最后一道防线。**
