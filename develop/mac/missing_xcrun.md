我的macOS操作系统，从 11.1 升级到 11.2 之后，发现运行一些工具命令，例如 `git` 出现报错:

```
xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing xcrun at: /Library/Developer/CommandLineTools/usr/bin/xcrun
```

这是因为 Xcode Command-line Tools 需要升级

- 打开一个终端窗口执行以下命令

```
xcode-select --install
```

- 在弹出窗口确认下载安装command line tools

- 安装完成后需要重启终端窗口程序

> 如果上述方式不成功，则尝试强制reset:

```bash
sudo xcode-select --reset
```

> 如果上述安装失败，则需要在WEB浏览器中登陆Apple Developer网站，通过web安装 `Command Line Tools for Xcode 12.x`

# 参考

* [Mac OS: xcrun: error: invalid active developer path, missing xcrun](https://ma.ttias.be/mac-os-xcrun-error-invalid-active-developer-path-missing-xcrun/)
* [Git is not working after macOS Update (xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools)](https://stackoverflow.com/questions/52522565/git-is-not-working-after-macos-update-xcrun-error-invalid-active-developer-pa)