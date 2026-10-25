# Lampa 应用构建

使用 GitHub Actions 自动构建 macOS 和 Windows 版本的 Lampa 应用。

## 特性

- ✅ **自动构建**：每次 push 到 main/master 分支时自动构建
- ✅ **双平台支持**：macOS (.dmg) 和 Windows (.zip)
- ✅ **双版本**：
  - **Local 版**：打包完整 Lampa 源代码，离线可用
  - **Online 版**：连接 http://lampa.mx 在线服务
- ✅ **自动发布**：推送 tag 时自动创建 GitHub Release

## 使用方法

### 1. 创建 Git 仓库并推送

```bash
cd /Users/aston/Documents/lampa
git init
git add .github/workflows/build.yml
git commit -m "Add GitHub Actions workflow for building Lampa apps

Co-Authored-By: Claude Opus 5.5 <noreply@anthropic.com>"

# 添加远程仓库
git remote add origin https://github.com/YOUR_USERNAME/lampa-app.git
git branch -M main
git push -u origin main
```

### 2. 查看构建进度

访问：`https://github.com/YOUR_USERNAME/lampa-app/actions`

### 3. 下载构建产物

构建完成后，在 Actions 页面的 "Artifacts" 部分下载：
- `macos-apps` - macOS DMG 文件
- `windows-apps` - Windows ZIP 文件

### 4. 发布正式版本

```bash
# 创建版本标签
git tag v1.0.0
git push origin v1.0.0
```

推送 tag 后，GitHub Actions 会自动创建 Release 并上传所有平台的安装包。

## 构建产物

### macOS
- **Lampa-Local-macOS.dmg** - 本地版 (~18MB)
  - 包含完整 Lampa 源代码
  - 无需网络即可使用
  
- **Lampa-Online-macOS.dmg** - 在线版 (~5MB)
  - 连接 http://lampa.mx
  - 需要网络连接

### Windows
- **Lampa-Local-Windows.zip** - 本地版
  - 解压后运行 `Lampa.bat`
  - 包含完整 Lampa 源代码
  
- **Lampa-Online-Windows.zip** - 在线版
  - 解压后运行 `Lampa.bat`
  - 连接 http://lampa.mx

## 技术栈

- **封装工具**: [webframe](https://github.com/tractordev/toolkit-go)
- **CI/CD**: GitHub Actions
- **macOS 渲染**: WebKit
- **Windows 渲染**: WebView2 (Edge)

## 手动触发构建

在 GitHub Actions 页面，选择 "Build Lampa Apps" workflow，点击 "Run workflow" 按钮。

## 本地测试

### macOS
```bash
# 构建后测试
open Lampa-Local.app
open Lampa-Online.app
```

### Windows
```cmd
# 解压后双击运行
Lampa.bat
```

## 注意事项

1. **Windows 用户**需要安装 [WebView2 Runtime](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)（Windows 10/11 通常已预装）
2. **macOS 用户**首次运行可能需要右键选择"打开"来绕过安全检查
3. 在线版需要网络连接到 http://lampa.mx

## 更新 Lampa 源代码

工作流会自动从 https://github.com/yumata/lampa 拉取最新代码，无需手动更新。
