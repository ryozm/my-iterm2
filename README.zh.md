# my-iterm2
我的 iterm2 配置步骤

[English](README.md) | [简体中文](README.zh.md)

## 截图
![截图](images/Snipaste1.png)

## 前提条件
系统：macOS
1. git（macOS 默认已安装 git）
2. zsh（macOS 默认已安装 zsh）

## 开始

### 安装 Nerd Fonts
1. 从[这里](https://www.nerdfonts.com/font-downloads)下载 Nerd Fonts（我使用 FiraCode Nerd Font）
2. 安装 Nerd Fonts

### 安装 iTerm2
1. 从[这里](https://www.iterm2.com/)下载 iTerm2
2. 安装 iTerm2
3. 将 iTerm2 字体设置为下载的 Nerd Fonts字体
  ```bash
  # 1. 打开 iTerm2
  # 2. 打开 Preferences（⌘ + ,）
  # 3. 进入 Profiles -> Text
  # 4. 将字体设置为下载的 Nerd Fonts字体
  ```
4. 将 iTerm2 颜色方案设置为此仓库中的方案（my-iterm2/iterm2-color-scheme.itermcolors）
  ```bash
  # 1. 打开 iTerm2
  # 2. 打开 Preferences（⌘ + ,）
  # 3. 进入 Profiles -> Colors
  # 4. 点击 Color Presets... -> Import...
  # 5. 选择 iterm2-color-scheme.itermcolors 文件
  # 6. 选择导入的颜色方案
  ```
5. 启用状态栏
  ```bash
  # 1. 打开 iTerm2
  # 2. 打开 Preferences（⌘ + ,）
  # 3. 进入 Profiles -> Session
  # 4. 勾选 Status bar enabled
  # 5. 点击 Configure Status Bar...
  # 6. 选择要显示的组件
  ```
6. 设置 iTerm2 外观
  ```bash
  # 1. 打开 iTerm2
  # 2. 打开 Preferences（⌘ + ,）
  # 3. 进入 Appearance -> General
  # 4. 将 Theme 设置为 Minimal
  # 5. 将 Tab bar location 设置为 Top
  # 6. 将 Status bar location 设置为 Bottom
  ```

### 安装 oh-my-zsh 和插件（zsh-autosuggestions, zsh-syntax-highlighting）
1. 从[这里](https://ohmyz.sh/#install)安装 oh-my-zsh
  ```bash
  # 快速安装
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```
2. 从[这里](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)安装 zsh-autosuggestions
  ```bash
  # 1. 在 oh-my-zsh 的插件目录中克隆此仓库：
  git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
  # 2. 在 ~/.zshrc 中的插件列表中添加该插件：
  plugins=( 
    # 其他插件...
    zsh-autosuggestions
  )
  # 3. 重新启动您的shell,查看效果
  ```
3. 从[这里](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)安装 zsh-syntax-highlighting
  ```bash
  # 1. 在 oh-my-zsh 的插件目录中克隆此仓库：
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  # 2. 在 ~/.zshrc 中的插件列表中添加该插件：
  plugins=( 
    # 其他插件...
    zsh-syntax-highlighting
  )
  # 3. 重新启动您的shell,查看效果
  ```


### 安装 Starship
1. 从[这里](https://starship.rs/guide/#%F0%9F%9A%80-installation)安装 Starship
  ```bash
  # 1. 使用 Shell 安装：
  sh -c "$(curl -fsSL https://starship.rs/install.sh)"
  # 2. 将初始化脚本添加到您的 shell 配置文件中：
  # Zsh
  echo 'eval "$(starship init zsh)"' >> ~/.zshrc
  ```
2. 配置 Starship
  ```bash
  # 1. 创建配置文件夹, 如果它不存在的话
  mkdir -p ~/.config
  # 4. 用此仓库中的 starship.toml 文件替换 starship.toml 文件
  mv my-iterm2/starship.toml ~/.config/starship.toml
  # 5. 重新启动您的shell,查看效果
  ```

### 安装 neofetch
首先需要从[这里](https://brew.sh/)安装 Homebrew
```bash
# 使用brew需要安装 Homebrew

# 1. 安装 neofetch
brew install neofetch
# 2. 将 neofetch 添加到 zshrc
echo 'neofetch' >> ~/.zshrc
# 3. 重新启动您的shell,查看效果
```

## 参考
1. [iTerm2](https://www.iterm2.com/)
2. [oh-my-zsh](https://ohmyz.sh/)
3. [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
4. [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
5. [Starship](https://starship.rs/)
6. [neofetch](https://github.com/dylanaraps/neofetch)
7. [FiraCode Nerd Font](https://www.nerdfonts.com/font-downloads)

## License
[MIT](LICENSE)