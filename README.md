# 糖果

本地音乐播放器（液态玻璃 UI · 多播放列表 · 内嵌/逐字歌词 · 随机可见顺序 · 长按调序）

## 云端打包（GitHub Actions）

1. 把本仓库推送到 GitHub 的 `main` 分支  
2. 打开 **Actions** → 选择 **Build 糖果 APK** → 等待绿色勾  
3. 点进本次运行 → **Artifacts** → 下载 **Candy-APK**  
4. 解压得到 `app-debug.apk`，安装到手机  

也可在 Actions 页点击 **Run workflow** 手动触发。

## 本地编译

```bash
# 需已安装 JDK 17 + Android SDK
echo "sdk.dir=/你的/Android/Sdk路径" > local.properties
gradle assembleDebug
# 产物: app/build/outputs/apk/debug/app-debug.apk
```

## 功能摘要

- 液态玻璃界面、沉浸状态栏  
- 歌词：同目录 LRC / 内嵌歌词 / 增强型逐字高亮  
- 随机播放时列表显示真实随机顺序  
- 长按歌曲：上移 / 下移 / 下一首 / 移除  
- 多播放列表互不干扰  
