# 配置 windows terminal 开发环境

windows terminal 简介

## settings

```json
{
    // ...
    "profiles":
    {
        // 全局通用的默认配置
        "defaults":
        {
            "fontFace": "Delugia Nerd Font",
            "fontSize": 10,
            // 光标样式 "vintage" ( ▃ ), "bar" ( ┃ ), "underscore" ( ▁ ), "filledBox" ( █ ), "emptyBox" ( ▯ )
            "cursorShape": "underscore",
            // 亚克力背板
            "useAcrylic": true,
            // 背板透明度
            "acrylicOpacity": 0.8
        },
        "list": [
            // 每一项配置一个shell
            {
                // 生成 guid 可以用 Powershell 命令 [guid]::NewGuid()
                "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
                "name": "Windows PowerShell",
                "commandline": "powershell.exe",
                // 工作目录
                "startingDirectory": ".",
                // 颜色样式
                "colorScheme": "Belafonte Night",
                "hidden": false
            },
        ]
    },
    "schemes": [
        // 每一项配置一个颜色样式
        // 可以到这里挑喜欢的 https://github.com/mbadolato/iTerm2-Color-Schemes/tree/master/windowsterminal
        {
            "name": "Belafonte Night",
            "black": "#20111b",
            "red": "#be100e",
            "green": "#858162",
            "yellow": "#eaa549",
            "blue": "#426a79",
            "purple": "#97522c",
            "cyan": "#989a9c",
            "white": "#968c83",
            "brightBlack": "#5e5252",
            "brightRed": "#be100e",
            "brightGreen": "#858162",
            "brightYellow": "#eaa549",
            "brightBlue": "#426a79",
            "brightPurple": "#97522c",
            "brightCyan": "#989a9c",
            "brightWhite": "#d5ccba",
            "background": "#20111b",
            "foreground": "#968c83"
        }
    ],
}
```

## oh-my-posh

<https://github.com/JanDeDobbeleer/oh-my-posh>

### 安装

```
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

### 使用

```
# Start the default settings
Set-Prompt
# Alternatively set the desired theme:
Set-Theme Agnoster
```

#### 解决乱码

[下载字体](./Delugia.Nerd.Font.Complete)，右键安装

## Terminal-Icons

<https://github.com/devblackops/Terminal-Icons>

### 安装

```
Install-Module -Name Terminal-Icons -Repository PSGallery
```

### 使用

```
Import-Module -Name Terminal-Icons
```

## scoop

<https://scoop.sh/>

### 安装

```
iwr -useb get.scoop.sh | iex
```

### 使用

```
scoop install vim
```

## 设置启动项

```
vim ~\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1
```
