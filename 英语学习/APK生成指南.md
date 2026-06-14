# 译林英语Quiz - 生成APK的三种方式

## 方式一：Gonative.io（最简单，推荐⭐）
1. 打开 https://gonative.io/
2. 输入一个在线URL（需要先把HTML上传到任意免费托管）
3. 或者点 "Code" 模式，上传HTML文件
4. 点击 "Build"，下载APK
- 免费，无需注册
- 支持全屏、状态栏颜色

## 方式二：PWABuilder（微软出品）
1. 先把HTML部署到任意免费托管（Vercel/GitHub Pages）
2. 打开 https://www.pwabuilder.com/
3. 输入你的网址，生成APK
- 免费且稳定

## 方式三：WebIntoApp.com（一键打包）
1. 打开 https://www.webintoapp.com/
2. 上传 quiz.html 或输入URL
3. 填写APP名称：译林英语Quiz
4. 选择图标，点击创建
5. 下载APK

## 方式四：HBuilderX 本地打包（需安装）
HBuilderX 云打包已不支持5+App项目，但可以：
1. 安装 HBuilderX
2. 新建 uni-app 项目
3. 在 pages/index/index.vue 中用 web-view 加载 quiz.html
4. 运行 → 运行到手机或模拟器

## 方式五：Android Studio（开发者）
见 android-app/ 目录下的完整项目，需要安装 Android Studio。
