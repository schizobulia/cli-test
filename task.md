# 需求

需要写一个github action自动下载hbuilderx的mac arm版本，然后自动编译一个示例项目。


# 资源

hbuilderx下载地址: https://download1.dcloud.net.cn/download/HBuilderX.5.13.2026061207-alpha.arm64.dmg

示例项目下载地址(尽可能快速下载alpha分支，不需要git clone全部): https://github.com/dcloudio/hello-uni-app-x

hbuilderx cli 参考文档：https://hx.dcloud.net.cn/cli/README

# hbuilderx编译命令

```bash
cli open # 打开hbuilderx

cli project open --path 项目路径 # 打开项目

cli launch app-android --project 项目名称 --compile true # 编译项目
```

# 注意

1、应该避免 GUI 弹窗阻塞 CI
2、避免mac出现:  “无法验证开发者、文件损坏” 的警告