# dotfile

My terminal looks like a garden. 🌹 🏘 🌱

## Screenshot

<div style="text-align:center"><img src ="https://raw.githubusercontent.com/wangshub/image-hosting/master/img/20190411090741.png" width="100%" /></div>


## Dependency

- iterm
- zsh
- oh-my-zsh 
- [iterm darkside theme](https://github.com/mbadolato/iTerm2-Color-Schemes/tree/master/schemes)
- ~~[powerlevel9k](https://github.com/bhilburn/powerlevel9k)~~ ,  `zsh-autosuggestions`这个插件可能有依赖， 不行再安装
- [powerlevel10k 打开命令行更加快](https://github.com/romkatv/powerlevel10k)
- [tmux config](https://github.com/samoshkin/tmux-config)
- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
- [colorls](https://github.com/athityakumar/colorls)
- [fzf](https://github.com/junegunn/fzf)

1.下载item2主题  

2.创建一个临时文件夹： TEMP , 
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git 

或
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k

```
下载文件夹， 整个文件夹移动到 ` ~/.oh-my-zsh/custom/themes/ `


3.
```
brew install tmux   
git clone https://github.com/samoshkin/tmux-config.git
$ ./tmux-config/install.sh  
```

4.创建一个临时文件夹： TEMP , git clone https://github.com/zsh-users/zsh-autosuggestions 下载文件夹(zsh-autosuggestions)， 整个文件夹移动到 ~/.oh-my-zsh/custom/plugins/
[
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

// ~/.zshrc 文件中添加， 如果有则直接写
plugins=(zsh-autosuggestions)
]

4.创建一个临时文件夹： TEMP , 
```
git clone https://github.com/zsh-users/zsh-autosuggestions 

```
下载文件夹(zsh-autosuggestions)， 整个文件夹移动到 ` ~/.oh-my-zsh/custom/plugins/ `

或
```
4.创建一个临时文件夹： TEMP , git clone https://github.com/zsh-users/zsh-autosuggestions 下载文件夹(zsh-autosuggestions)， 整个文件夹移动到 ~/.oh-my-zsh/custom/plugins/
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

// ~/.zshrc 文件中添加， 如果有则直接写
plugins=(zsh-autosuggestions)

下面需要操作，否则出不来； 无效
Clone this repository somewhere on your machine. This guide will assume ~/.zsh/zsh-autosuggestions.

git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
Add the following to your .zshrc:

source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
Start a new terminal session.

```

5.

```
brew install zsh-syntax-highlighting

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc

~/.zshrc （记得检查路径）
写上 source ./zsh-syntax-highlighting/zsh-syntax-highlighting.zsh

```

6.
```
brew tap homebrew/cask-fonts
brew cask install font-hack-nerd-font

> Note for iTerm2 users - Please enable the Nerd Font at iTerm2 > Preferences > Profiles > Text > Non-ASCII font > Hack Regular Nerd Font Complete.

sudo gem install colorls
```


7.
Using Homebrew or Linuxbrew
You can use Homebrew or Linuxbrew to install fzf.
```
brew install fzf

To install useful key bindings and fuzzy completion:
$(brew --prefix)/opt/fzf/install

````
fzf is also available via MacPorts: sudo port install fzf

或 Using git
Alternatively, you can "git clone" this repository to any directory and run install script.
```
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

## Install 

```shell
git clone https://github.com/wangshub/dotfile.git

cd dotfile

./install.sh
```

最后修改 ~/.zshrc文件中的  /Users/kaboom 中的kaboom成你电脑路径


~/.bash_profile 文件内容
```
export PUB_HOSTED_URL=https://pub.flutter-io.cn 
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn 
#export FLUTTER_STORAGE_BASE_URL="https://mirrors.tuna.tsinghua.edu.cn/flutter"
export PATH=/Users/pro/NiuB/flutter/bin:$PATH

JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_181.jdk/Contents/Home
PATH=$JAVA_HOME/bin:$PATH:.
CLASSPATH=$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar:.
export JAVA_HOME
export PATH
export CLASSPATH

#export ANDROID_HOME=/Users/pro/Library/Android/sdk
#export PATH=${PATH}:${ANDROID_HOME}/platform-tools
#export PATH=${PATH}:${ANDROID_HOME}/tools
#export PATH=${PATH}:${ANDROID_HOME}/build-tools/28.0.3


#直接关闭brew每次执行命令时的自动更新（推荐）
export HOMEBREW_NO_AUTO_UPDATE=true

export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles

[[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm" # Load RVM into a shell session *as a function*
```

## License

MIT @ [wangshub](https://github.com/wangshub)
