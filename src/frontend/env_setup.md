# Frontend
## 前言

最近公司电脑换代，公司配了16寸新mbp，原15寸mbp自购后将硬盘全部清理后自用，意味着我要装机2次，程序员的电脑装机意味着大量的配置、软件、插件都要进行设置，还很容易遗漏，在装一个机器后，装第二个机器前专门整理一下并分享出来供大家参考，我是前端程序员所以可能部分内容更适合于前端，大家自行取舍。

## 基本内容

### git

在mac终端输入git命令会提示你安装xcode，但是xcode非常大，前端程序员也不太需要，所以大家可以通过下面命令只安装git。

csharp

复制代码

`$ xcode-select --install $ git init`

#### 加速

没有网络相关问题的忽略该小节

自己改一下host配置，会有提升但实在有限，还是建议买vpn

sql

复制代码

`# GitHub Start 52.74.223.119 github.com 192.30.253.119 gist.github.com 54.169.195.247 api.github.com 185.199.111.153 assets-cdn.github.com 151.101.76.133 raw.githubusercontent.com 151.101.108.133 user-images.githubusercontent.com 151.101.76.133 gist.githubusercontent.com 151.101.76.133 cloud.githubusercontent.com 151.101.76.133 camo.githubusercontent.com 151.101.76.133 avatars0.githubusercontent.com 151.101.76.133 avatars1.githubusercontent.com 151.101.76.133 avatars2.githubusercontent.com 151.101.76.133 avatars3.githubusercontent.com 151.101.76.133 avatars4.githubusercontent.com 151.101.76.133 avatars5.githubusercontent.com 151.101.76.133 avatars6.githubusercontent.com 151.101.76.133 avatars7.githubusercontent.com 151.101.76.133 avatars8.githubusercontent.com # GitHub End`

很多人通过设置ip的方式解决速度慢的问题，但是很多时候即使设置了ip但是clone还是很慢，这里我推荐下面的方法比较好用。

可以将本来的

bash

复制代码

`git clone https://github.com/xxx.git`

改成：

bash

复制代码

`git clone https://github.com.cnpmjs.org/xxx.git`

### 我的配置文件

先将一些配置信息clone下来，通过一些脚本的形式帮助快速安装（这套配置是我团队 **风乘** 大神的配置信息,我fork下来进行了部分修改，如果有定制需求可以将其fork下来进行修改使用）

shell

复制代码

`$ git clone https://github.com/wang516038746/dot-files.git $ cd dot-files $ chmod +x *.sh`

### ssh

新的电脑, 新的 ssh key，执行后输入密码即可

perl

复制代码

`$ ssh-keygen -t rsa -C "youremail@example.com"`

### brew

进入clone下来的dot-files文件

matlab

复制代码

`// 如果当前目录已经是 dot-files 忽略 cd dot-files`

安装homebrew  
直接使用[homebrew](https://link.juejin.cn?target=https%3A%2F%2Fbrew.sh%2F "https://brew.sh/")提供的地址，可能会被墙或者很慢  
你可以通过我的配置安装，使用前确保你在我的dot-files目录中

bash

复制代码

`/bin/bash ./brew_install`

**(不保证100%成功，如果没有成功，请自行找其他方法安装) **  
_我个人使用的时候经常在这一步卡住_ ![](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/57772d3736fe401d9031748dfa9c6288~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp) ctrl+c 关闭重新来即可，已下载过部分下载的会很快 ，如果重来时出现这个报错 ![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b963e1eab3b94d8a9148f10359cf7243~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp) 先执行以下面命令， yourname 替换成你的文件夹名字

shell

复制代码

`$ rm /Users/youname/Library/Caches/Homebrew/portable-ruby-2.6.3_2.yosemite.bottle.tar.gz $ /bin/bash ./brew_install`

### iTerm2

直接通过[iTerm2官网](https://link.juejin.cn?target=https%3A%2F%2Fwww.iterm2.com%2Findex.html "https://www.iterm2.com/index.html") 下载解压使用即可 ![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/4b1b3c166b29498e8cccd98bb14a5c2b~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

#### iterm2调校

配置

shell

复制代码

`$ cp iterm2 ~/Library/Application\ Support/iTerm2/DynamicProfiles/`

设置生效

重启 iterm2 后在 `Preferences > Profiles` 界面应该就能看见导入的配置了

额外快捷键:

- alt + → : 光标右移一个单词
- alt + ← : 光标右移一个单词
- alt + del: 删除一个单词

一些设置，可以参考

![](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b34eb57e39cf4e5286a3c87e290bb824~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/5cfae8f0614245538de9361cd3c194e6~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

#### zsh

安装[oh-my-zsh](https://link.juejin.cn?target=https%3A%2F%2Fohmyz.sh%2F "https://ohmyz.sh/")

ruby

复制代码

`$ sh zsh_install.sh` 

安装高亮插件

ruby

复制代码

`$ git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`

zsh配置

shell

复制代码

`$ cp .zshrc ~/.zshrc $ source ~/.zshrc`

### vim

我用 [SpaceVim](https://link.juejin.cn?target=https%3A%2F%2Fspacevim.org%2Fcn%2Fquick-start-guide%2F%23linux-%25E6%2588%2596-macos "https://spacevim.org/cn/quick-start-guide/#linux-%E6%88%96-macos")

ruby

复制代码

`$ curl -sLf https://spacevim.org/cn/install.sh | bash -s -- -h`

建议重装下 vim, 覆盖系统 vim

ruby

复制代码

`$ brew reinstall vim`

`SpaceVim` 配置

shell

复制代码

`$ cp .space-vim.toml ~/.SpaceVim.d/init.toml`

### nvm

node 版本管理强推 [nvm](https://link.juejin.cn?target=https%3A%2F%2Fgithub.com%2Fcreationix%2Fnvm%2Fblob%2Fmaster%2FREADME.md "https://github.com/creationix/nvm/blob/master/README.md")

bash

复制代码

`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash`

nvm 懒加载, 提高 zsh 第一次打开速度, 请根据实际情况选择添加, 会影响默认 nvm 指令, 替换 nvm 放入 zshrc 中的内容即可(已经执行过 `cp .zshrc ~/.zshrc`可忽略 )

bash

复制代码

`export PATH="~/.nvm/versions/node/v10.14.2/bin:$PATH" nvm(){    unfunction "nvm"    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"   # This loads nvm    [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_↷    nvm "$@" }`

#### node npm

ruby

复制代码

`$ nvm install 10 $ nvm alias default 10`

安装 npm 全局依赖, 安装列表见文件 `brew-casks`

shell

复制代码

`$ ./npm.sh $ nrm use taobao`

#### yarn

使用 brew 安装 yarn

css

复制代码

`$ brew install yarn --without-node`

#### brew安装其他软件

通过brew安装软件, 建议最后安装, 安装列表见文件 `brew-casks`

shell

复制代码

`$ ./brew.sh`

#### 字体

[homebrew-cask-fonts](https://link.juejin.cn?target=https%3A%2F%2Fgithub.com%2FHomebrew%2Fhomebrew-cask-fonts "https://github.com/Homebrew/homebrew-cask-fonts")

shell

复制代码

`$ brew tap homebrew/cask-fonts`

字体推荐 `Fira Code`

css

复制代码

`$ brew cask install font-fira-code $ brew cask install font-meslo-for-powerline $ brew cask install font-sarasa-gothic          # 更纱黑体`

## 工具类软件

### vscode

[vscode](https://link.juejin.cn?target=https%3A%2F%2Fcode.visualstudio.com%2F "https://code.visualstudio.com/")

通过code命令启动vscode  
打开 Command + shift + p 输入 shell

![](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/2f1637c5398b4bd3896d027a94088cc7~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

迁移插件及配置信息  
通过 Settings Sync 扩展

### 浏览器

chrome 浏览器  
google账号可以把包括浏览记录在内的所有信息迁移

Microsoft Edge  
这个真的香，谁用谁知道，反正我除了工作时用chrome，业余活动都用Edge

### snipaste

截图神器, [snipaste官网](https://link.juejin.cn?target=https%3A%2F%2Fzh.snipaste.com%2F "https://zh.snipaste.com/")

设置文件

shell

复制代码

`$ cp .snipaste ~/.snipaste/config.ini`

快捷键

- ⌘ + ⌃ + a : 截图

### paste

拷贝粘贴神器  
会记录你复制的历史 ⌘ + shift + v 选择粘贴内容