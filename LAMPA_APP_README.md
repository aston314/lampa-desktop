# Lampa 应用使用说明

## ✅ 已完成任务

### 1. 自定义图标
- ✅ 创建了 Lampa 品牌图标（橙色灯泡 + Play 按钮）
- ✅ 已应用到两个应用版本
- 图标文件：`/tmp/lampa.icns`

### 2. 本地 Lampa 部署
- ✅ 克隆了 Lampa 源代码到：`/Users/aston/Documents/lampa/lampa-source`
- ✅ 启动了本地 HTTP 服务器：`http://127.0.0.1:8080`
- ✅ 创建了连接本地服务的应用：`Lampa-Local.app`

---

## 📦 应用版本

### Lampa.app（在线版）
- **位置：** `/Users/aston/Downloads/Lampa.app`
- **连接：** `http://lampa.mx`（在线服务）
- **特点：** 无需本地服务器，直接使用
- **图标：** ✅ 已应用自定义图标

### Lampa-Local.app（本地版）
- **位置：** `/Users/aston/Downloads/Lampa-Local.app`
- **连接：** `http://127.0.0.1:8080`（本地服务器）
- **特点：** 完全本地运行，可以修改代码
- **图标：** ✅ 已应用自定义图标

---

## 🚀 使用方法

### 在线版（简单）
```bash
# 直接双击启动
open /Users/aston/Downloads/Lampa.app
```

### 本地版（需要先启动服务器）
```bash
# 1. 启动本地服务器
cd /Users/aston/Documents/lampa/lampa-source
python3 -m http.server 8080

# 2. 然后双击启动应用
open /Users/aston/Downloads/Lampa-Local.app
```

**或者使用自动启动脚本：**
```bash
# 在后台启动服务器并打开应用
cd /Users/aston/Documents/lampa/lampa-source && \
python3 -m http.server 8080 >/tmp/lampa_server.log 2>&1 & \
sleep 2 && open /Users/aston/Downloads/Lampa-Local.app
```

---

## 📁 目录结构

```
/Users/aston/Documents/lampa/
├── lampa-source/          # Lampa 源代码
│   ├── index.html        # 主页面
│   ├── app.min.js        # 应用逻辑
│   ├── css/              # 样式文件
│   ├── img/              # 图片资源
│   └── lang/             # 多语言文件
│
/Users/aston/Downloads/
├── Lampa.app             # 在线版应用（http://lampa.mx）
└── Lampa-Local.app       # 本地版应用（localhost:8080）
```

---

## 🎨 自定义开发

### 修改 Lampa 界面
```bash
cd /Users/aston/Documents/lampa/lampa-source

# 编辑 HTML
vim index.html

# 编辑样式
vim css/app.css

# 修改后刷新浏览器即可看到效果
```

### 更新图标
```bash
# 替换图标文件
cp /path/to/new_icon.icns /Users/aston/Downloads/Lampa.app/Contents/Resources/lampa.icns

# 刷新 Finder 缓存
touch /Users/aston/Downloads/Lampa.app
killall Finder
```

---

## 🔧 技术栈

- **封装工具：** webframe（Go + WebKit）
- **应用大小：** ~5MB（比 Electron 轻 30 倍）
- **渲染引擎：** macOS 原生 WebKit
- **开发工具：** 已启用（右键检查元素）

---

## 📝 服务器管理

### 查看本地服务器状态
```bash
lsof -i :8080
```

### 停止本地服务器
```bash
pkill -f "python3 -m http.server 8080"
```

### 查看服务器日志
```bash
tail -f /tmp/lampa_server.log
```

---

## 🎯 后续步骤

### 安装到应用程序文件夹
```bash
# 在线版
cp -r /Users/aston/Downloads/Lampa.app /Applications/

# 本地版
cp -r /Users/aston/Downloads/Lampa-Local.app /Applications/
```

### 创建 Windows 版本
webframe 也支持 Windows，可以用同样的方法创建 Windows 应用。

### 使用真实的 Lampa 图标
如果有 Lampa 官方的高清图标文件，可以替换当前的自定义图标：
```bash
# 转换 PNG/SVG 为 icns
# 然后复制到 Resources 文件夹
```

---

## ⚠️ 注意事项

1. **本地版需要服务器运行：** Lampa-Local.app 必须先启动 HTTP 服务器才能使用
2. **端口占用：** 确保 8080 端口没有被其他程序占用
3. **首次运行：** macOS 可能提示"无法验证开发者"，右键选择"打开"即可

---

## 🎉 完成情况

- ✅ 任务 1：添加自定义图标
- ✅ 任务 3：克隆本地 Lampa 仓库并创建本地应用

**两个应用都已就绪，可以直接使用！**
