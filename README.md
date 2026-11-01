# 蜗牛速递 SnailDrop

make updating greating

**已停止维护的实验性项目，发布源码供学习和研究。**

本项目尝试在 macOS 中读取百度网盘客户端所选文件，再由自己的下载引擎传输。开发版本为 0.4.2；Windows 和 Android 尚未实现。

## 当前状态

项目没有达到稳定、高速下载的目标。部分文件曾成功传输，也验证过文件夹展开和部分断点续传；仍可能遇到授权、接口拒绝、网络超时与长时间稳定性问题。**不承诺可用、稳定或不限速，不作为成熟下载器推荐。**

## 获取完整源码

本次通过 GitHub 网页发布，完整目录结构保存在 [SnailDrop-source-0.4.2.zip](SnailDrop-source-0.4.2.zip) 中。解压后包含 macOS Swift 源码、前端、测试、构建脚本、详细 README、开发计划和历史验收记录。压缩包的 SHA-256 见 [SHA256SUMS.txt](SHA256SUMS.txt)。

构建需要 macOS 与 Xcode Command Line Tools。在解压后的 SnailDrop 目录执行：

```sh
./scripts/build-macos.sh
```

产物位于 `dist/SnailDrop.app`，使用本机临时签名，未公证。源码中的路径与 bundle identifier 沿用早期 CloudHarbor 命名。请先阅读压缩包内 README 中的辅助功能权限、独立网页登录、临时日志和本机任务数据说明。

## 发布内容

只包含源码、测试与文档；不包含登录会话、Cookie、访问令牌、分享链接、下载记录、下载文件或本机编译产物。不要将自己的凭据或任务数据提交到公开仓库。

## 参考

功能方向参考 [PanDL](https://github.com/MoyerZhang-Claude/cloud-drive-link-parsing)，协议调研包括 [BaiduPCS-Go](https://github.com/qjfoidnh/BaiduPCS-Go) 与 [LinkSwift](https://github.com/hmjz100/LinkSwift)。未复制这些项目的实现代码；具体调研与测试局限见源码包内 docs。

原创源码采用 [MIT License](LICENSE)。
