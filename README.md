# 🌊 AudioTerrain (桌面音频地貌) for macOS

[![Platform](https://img.shields.io/badge/platform-macOS-black.svg)](https://apple.com)
[![Metal](https://img.shields.io/badge/Render-Metal--API-blue.svg)](https://developer.apple.com/metal/)
[![Swift](https://img.shields.io/badge/Language-Swift--5.0-orange.svg)](https://swift.org)

AudioTerrain 是一款运行在 macOS 菜单栏的高性能、低能耗的 3D 原生音频反应动态壁纸。它基于 Apple Metal 图形 API 构建，能够与您系统播放的任何音乐、视频或环境音实时同步，渲染出高帧率的 3D 波形地貌景观。

---

## ✨ 核心特性

- **🚀 原生 Metal 驱动**：底层完全基于 Apple Metal 3D 图形引擎打造，GPU 零延迟响应，相比传统 Electron 或 Web 动态壁纸降低了 90% 的 CPU 损耗。
- **📺 视网膜级原生渲染 (HiDPI)**：支持 macOS Retina 原生像素点对点输出，网格线与线条边缘清晰逼真。
- **🪄 完美的着色器级抗锯齿 (Shader AA)**：内置屏幕空间导数几何抖动消除技术，旋转视角或远景毫无像素颗粒与闪烁。
- **⚡ 后台多线程分离渲染 (CVDisplayLink)**：渲染回路完全移至后台专用硬件同步线程，即使您点击设置、拖拽窗口或进行繁重布局，壁纸也永远保持满帧（60/120 FPS）丝滑运行，绝对不卡顿。
- **🔋 零能耗自动休眠模式 (Zero-Footprint)**：在音乐停止或系统静音时，壁纸渲染会自动完全暂停并释放 GPU 算力，恢复播放时毫秒级自动唤醒，极致省电。
- **🎨 丰富的主题与微调**：内置 10 款艺术色调主题（深夜守护、深海物语、极地极光等），支持调整采集灵敏度、旋转速度、涟漪特效与特效粒子参数。

---

## 📦 如何下载与安装

### 下载正式版
1. 点击本仓库右侧的 **[Releases]** 区域。
2. 下载最新版本的 `AudioTerrainMetal.app.zip`。
3. 双击解压，将得到的 `AudioTerrainMetal.app` 拖入您的 **应用程序 (Applications)** 文件夹。

### 首次运行配置与授权
由于 macOS 系统安全机制，首次打开需要完成以下设置：
1. **屏幕录制权限**：动态壁纸需要获取当前屏幕的像素布局并绘制到桌面层，首次运行会弹出权限请求，请在 `系统设置 -> 隐私与安全性 -> 屏幕录制` 中为 `AudioTerrainMetal` 勾选授权。
2. **麦克风/音频输入权限**：用于采集播放的音乐波形。请在首次弹窗中允许访问。若使用全局音乐同步，建议安装虚拟音频线驱动（如 BlackHole）并设置为输入源。

---

## ⚙️ 常见问题与支持
如果您在使用中遇到问题，或者有任何功能建议，欢迎在本仓库的 **[Issues]** 页面提交反馈。
