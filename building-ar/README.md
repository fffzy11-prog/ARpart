# 最小 MindAR + A-Frame 建筑 AR

纯静态网页，无需 npm 安装或构建。依赖 A-Frame 1.6.0 和 MindAR 1.2.5 CDN，需要联网。

## 手机测试

1. 将本文件夹中的 index.html 和 assets 整体上传到支持 HTTPS 的静态托管服务（例如 GitHub Pages）。保持目录结构。
2. 手机使用 Safari（iPhone）或 Chrome（Android）打开部署后的 HTTPS 地址，允许相机权限。避免微信内置浏览器。
3. 在电脑上打开 assets/target.png，或打印出来。手机扫描这张图。识别后显示透明背景建筑，移动或转动识别图，建筑随之移动；丢失识别图时隐藏。

不能直接双击 HTML 或用手机访问 http://电脑局域网IP 来测试相机。若使用本地开发服务器，需要通过 HTTPS 隧道访问，并把项目文件夹作为网站根目录。

## 换成自己的图片

- 将自己的透明背景建筑图片保存为 assets/building.png。当前附带的是程序绘制的透明建筑示意图。
- 若 PNG 不是正方形，把 index.html 中 a-image 的 height 改为 图片高度/图片宽度（width 保持 1）。
- 打开 https://hiukim.github.io/mind-ar-js-doc/tools/compile/ ，上传你要扫描的识别图，编译并下载 .mind，替换 assets/targets.mind。只上传一张图，对应 targetIndex: 0。
- assets/target.png 只是给人查看的识别图；更换它不会自动更新识别数据，必须重新编译 .mind。
- 当前为跟随识别图的二维 PNG 平面，不是立体建筑模型。position 的第三个值控制离识别图平面的距离。

## 官方参考

- https://github.com/hiukim/mind-ar-js （README）
- https://hiukim.github.io/mind-ar-js-doc/quick-start/overview/
- https://hiukim.github.io/mind-ar-js-doc/examples/basic/

沿用官方 card.png / card.mind 配对测试资源；仓库采用 MIT 许可。尚未进行真实手机相机测试。
