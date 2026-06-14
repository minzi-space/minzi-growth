# 译林英语Quiz - Android APK 构建指南

## 项目结构
```
android-app/
├── app/
│   ├── build.gradle
│   ├── proguard-rules.pro
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── assets/
│       │   └── quiz.html          ← 核心 HTML 文件
│       ├── java/com/yilin/quiz/
│       │   ├── MainActivity.kt    ← WebView 主界面
│       │   └── SplashActivity.kt  ← 启动页
│       └── res/
│           ├── layout/activity_splash.xml
│           └── values/
│               ├── strings.xml
│               └── themes.xml
├── build.gradle
├── settings.gradle
└── gradle/wrapper/gradle-wrapper.properties
```

## 构建方式

### 方式一：Android Studio（推荐）
1. 安装 [Android Studio](https://developer.android.com/studio)
2. 打开项目：File → Open → 选择 `android-app` 文件夹
3. 等待 Gradle 同步完成
4. Build → Build Bundle(s) / APK(s) → Build APK(s)
5. APK 输出路径：`app/build/outputs/apk/debug/app-debug.apk`

### 方式二：命令行
```bash
cd android-app
./gradlew assembleDebug
# APK 位于 app/build/outputs/apk/debug/app-debug.apk
```

### 方式三：在线构建（无需安装 Android Studio）
使用 [GitHub Actions](https://github.com/features/actions) 或 [Appetize](https://appetize.io/) 在线构建。

## 更新 HTML 内容
只需要替换 `app/src/main/assets/quiz.html` 文件，然后重新构建即可。

## 功能特性
- WebView 全屏沉浸式体验
- 启动页 splash screen
- 返回键支持（WebView 内回退）
- 状态栏/导航栏透明适配
- 多用户登录，数据按用户隔离存储
- DOM Storage 支持（localStorage）
