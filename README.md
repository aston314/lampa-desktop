# Lampa Desktop

[English](#english) | [简体中文](#简体中文) | [Русский](#русский) | [Українська](#українська)

---

## English

Automatically build macOS and Windows versions of Lampa desktop application using GitHub Actions.

### Features

- ✅ **Automatic builds**: Auto-build on every push to main branch
- ✅ **Cross-platform**: macOS (.dmg) and Windows (.zip)
- ✅ **Two versions**:
  - **Local**: Bundled with complete Lampa source code, works offline
  - **Online**: Connects to http://lampa.mx
- ✅ **Auto-release**: Automatically creates GitHub Release when you push a tag

### Download

Visit [Releases](https://github.com/aston314/lampa-desktop/releases) to download the latest version.

### Build Output

#### macOS
- **Lampa-Local-macOS.dmg** - Local version (~18MB)
  - Includes complete Lampa source code
  - Works without internet connection
  
- **Lampa-Online-macOS.dmg** - Online version (~5MB)
  - Connects to http://lampa.mx
  - Requires internet connection

#### Windows
- **Lampa-Local-Windows.zip** - Local version
  - Run `Lampa.bat` after extraction
  - Includes complete Lampa source code
  
- **Lampa-Online-Windows.zip** - Online version
  - Run `Lampa.bat` after extraction
  - Connects to http://lampa.mx

### Tech Stack

- **Wrapper**: [webframe](https://github.com/tractordev/webframe)
- **CI/CD**: GitHub Actions
- **macOS Renderer**: WebKit
- **Windows Renderer**: WebView2 (Edge)

### Notes

1. **Windows users** need [WebView2 Runtime](https://developer.microsoft.com/en-us/microsoft-edge/webview2/) (usually pre-installed on Windows 10/11)
2. **macOS users** may need to right-click and select "Open" on first launch
3. Online version requires connection to http://lampa.mx
4. Lampa source is automatically fetched from https://github.com/yumata/lampa

---

## 简体中文

使用 GitHub Actions 自动构建 macOS 和 Windows 版本的 Lampa 桌面应用。

### 特性

- ✅ **自动构建**：每次 push 到 main 分支时自动构建
- ✅ **跨平台支持**：macOS (.dmg) 和 Windows (.zip)
- ✅ **双版本**：
  - **本地版**：打包完整 Lampa 源代码，离线可用
  - **在线版**：连接 http://lampa.mx 在线服务
- ✅ **自动发布**：推送 tag 时自动创建 GitHub Release

### 下载

访问 [Releases](https://github.com/aston314/lampa-desktop/releases) 下载最新版本。

### 构建产物

#### macOS
- **Lampa-Local-macOS.dmg** - 本地版 (~18MB)
  - 包含完整 Lampa 源代码
  - 无需网络即可使用
  
- **Lampa-Online-macOS.dmg** - 在线版 (~5MB)
  - 连接 http://lampa.mx
  - 需要网络连接

#### Windows
- **Lampa-Local-Windows.zip** - 本地版
  - 解压后运行 `Lampa.bat`
  - 包含完整 Lampa 源代码
  
- **Lampa-Online-Windows.zip** - 在线版
  - 解压后运行 `Lampa.bat`
  - 连接 http://lampa.mx

### 技术栈

- **封装工具**: [webframe](https://github.com/tractordev/webframe)
- **CI/CD**: GitHub Actions
- **macOS 渲染**: WebKit
- **Windows 渲染**: WebView2 (Edge)

### 注意事项

1. **Windows 用户**需要安装 [WebView2 Runtime](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)（Windows 10/11 通常已预装）
2. **macOS 用户**首次运行可能需要右键选择"打开"来绕过安全检查
3. 在线版需要网络连接到 http://lampa.mx
4. 工作流会自动从 https://github.com/yumata/lampa 拉取最新代码

---

## Русский

Автоматическая сборка настольного приложения Lampa для macOS и Windows с помощью GitHub Actions.

### Особенности

- ✅ **Автоматическая сборка**: Автосборка при каждом push в ветку main
- ✅ **Кроссплатформенность**: macOS (.dmg) и Windows (.zip)
- ✅ **Две версии**:
  - **Локальная**: Со встроенным исходным кодом Lampa, работает офлайн
  - **Онлайн**: Подключается к http://lampa.mx
- ✅ **Автоматический релиз**: Автоматически создает GitHub Release при push тега

### Загрузка

Посетите [Releases](https://github.com/aston314/lampa-desktop/releases) для загрузки последней версии.

### Результаты сборки

#### macOS
- **Lampa-Local-macOS.dmg** - Локальная версия (~18MB)
  - Включает полный исходный код Lampa
  - Работает без интернета
  
- **Lampa-Online-macOS.dmg** - Онлайн версия (~5MB)
  - Подключается к http://lampa.mx
  - Требуется подключение к интернету

#### Windows
- **Lampa-Local-Windows.zip** - Локальная версия
  - Запустите `Lampa.bat` после распаковки
  - Включает полный исходный код Lampa
  
- **Lampa-Online-Windows.zip** - Онлайн версия
  - Запустите `Lampa.bat` после распаковки
  - Подключается к http://lampa.mx

### Технологический стек

- **Обертка**: [webframe](https://github.com/tractordev/webframe)
- **CI/CD**: GitHub Actions
- **Рендеринг macOS**: WebKit
- **Рендеринг Windows**: WebView2 (Edge)

### Примечания

1. **Пользователям Windows** требуется [WebView2 Runtime](https://developer.microsoft.com/en-us/microsoft-edge/webview2/) (обычно предустановлен в Windows 10/11)
2. **Пользователям macOS** может потребоваться щелкнуть правой кнопкой мыши и выбрать "Открыть" при первом запуске
3. Онлайн версия требует подключения к http://lampa.mx
4. Исходный код Lampa автоматически загружается из https://github.com/yumata/lampa

---

## Українська

Автоматична збірка настільного додатку Lampa для macOS та Windows за допомогою GitHub Actions.

### Особливості

- ✅ **Автоматична збірка**: Автозбірка при кожному push до гілки main
- ✅ **Крос-платформність**: macOS (.dmg) та Windows (.zip)
- ✅ **Дві версії**:
  - **Локальна**: Зі вбудованим вихідним кодом Lampa, працює офлайн
  - **Онлайн**: Підключається до http://lampa.mx
- ✅ **Автоматичний реліз**: Автоматично створює GitHub Release при push тегу

### Завантаження

Відвідайте [Releases](https://github.com/aston314/lampa-desktop/releases) для завантаження останньої версії.

### Результати збірки

#### macOS
- **Lampa-Local-macOS.dmg** - Локальна версія (~18MB)
  - Включає повний вихідний код Lampa
  - Працює без інтернету
  
- **Lampa-Online-macOS.dmg** - Онлайн версія (~5MB)
  - Підключається до http://lampa.mx
  - Потрібне підключення до інтернету

#### Windows
- **Lampa-Local-Windows.zip** - Локальна версія
  - Запустіть `Lampa.bat` після розпакування
  - Включає повний вихідний код Lampa
  
- **Lampa-Online-Windows.zip** - Онлайн версія
  - Запустіть `Lampa.bat` після розпакування
  - Підключається до http://lampa.mx

### Технологічний стек

- **Обгортка**: [webframe](https://github.com/tractordev/webframe)
- **CI/CD**: GitHub Actions
- **Рендеринг macOS**: WebKit
- **Рендеринг Windows**: WebView2 (Edge)

### Примітки

1. **Користувачам Windows** потрібен [WebView2 Runtime](https://developer.microsoft.com/en-us/microsoft-edge/webview2/) (зазвичай попередньо встановлений у Windows 10/11)
2. **Користувачам macOS** може знадобитися клацнути правою кнопкою миші та вибрати "Відкрити" при першому запуску
3. Онлайн версія потребує підключення до http://lampa.mx
4. Вихідний код Lampa автоматично завантажується з https://github.com/yumata/lampa
