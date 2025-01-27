---
title: 設定「主要」的「按鍵綁定」
nav_order: 7010
has_children: false
parent: 設定「按鍵綁定 (Keybind)」
grand_parent: 如何
---


# 設定「主要」的「按鍵綁定」




## 主題

* [前提](#前提)
* [設定範例](#設定範例)
* [統整](#統整)
* [範例腳本](#範例腳本)




## 前提

延續「[設定「按鍵綁定 (Keybind)」](https://samwhelp.github.io/note-about-ubuntu-budgie/read/howto/config-keybind.html)」這篇找到的設定，

以下紀錄我常用的「視窗操作按鍵綁定」來當作「[設定範例](#設定範例)」說明。

> 要注意的是，以下只是單就個別項目做說明，有些綁定可能會跟目前既有的綁定衝突，所以要設定完整，還是要做統整的設定
以下紀錄並不完全。




## 設定範例

* [Window / Close](#window--close)
* [Window / Toggle Maximized](#window--toggle-maximized)
* [Window / Toggle Fullscreen](#window--toggle-fullscreen)
* [Window / Show Desktop](#window--show-desktop)
* [Window / Begin Move](#window--begin-move)
* [Window / Begin Resize](#window--begin-resize)
* [Alt-Tab Switcher](#alt-tab-switcher)
* [Window / Previous](#window--previous)
* [Window / Next](#window--next)
* [Workspace / Previous](#workspace--previous)
* [Workspace / Next](#workspace--next)
* [Window / Tiling Move](#window--tiling-move)
* [Screenshot](#screenshot)
* [統整](#統整)




## Window / Close

大部份的桌面環境，預設是綁定「`Alt + F4`」來「關閉視窗」。

```
org.gnome.desktop.wm.keybindings close ['<Alt>F4']
```

我個人慣用的是綁定「`Win + q`」來「關閉視窗」。


> 執行下面指令，綁定「`Win + q`」來「關閉視窗」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings close "['<Super>q']"
```


> 或是也可以執行下面指令，綁定「`Win + q`」來「關閉視窗」，並且也保留原來的「`Alt + F4`」綁定。

``` sh
gsettings set org.gnome.desktop.wm.keybindings close "['<Super>q', '<Alt>F4']"
```

> 上面的範例，表示一個功能，可以有多重綁定。




## Window / Toggle Maximized

> 執行下面指令，綁定「`Win + w`」來「切換視窗最大化」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings toggle-maximized "['<Super>w']"
```




## Window / Toggle Fullscreen

> 執行下面指令，綁定「`Win + f`」來「切換視窗全螢幕」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings toggle-fullscreen "['<Super>f']"
```




## Window / Show Desktop

> 在「Ubuntu Gnome Shell」，預設就是綁定「`Win + d`」來「切換顯示桌面」。

```
org.gnome.desktop.wm.keybindings show-desktop ['<Primary><Super>d', '<Primary><Alt>d', '<Super>d']
```

> 執行下面指令，綁定「`Win + d`」來「切換顯示桌面」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings show-desktop "['<Super>d']"
```




## Window / Begin Move

> 執行下面指令，綁定「`Win + e`」來切換到「視窗開始移動」狀態。

``` sh
gsettings set org.gnome.desktop.wm.keybindings begin-move "['<Super>e']"
```




## Window / Begin Resize

> 執行下面指令，綁定「`Win + r`」來切換到「視窗開始更改大小」狀態。

``` sh
gsettings set org.gnome.desktop.wm.keybindings begin-resize "['<Super>r']"
```


> 關於「[begin-move](#window--begin-move)」和「[begin-resize](#window--begin-resize)」，可以對照另一篇『[設定「Mouse Button Modifier」](https://samwhelp.github.io/note-about-ubuntu-budgie/read/howto/config-mouse-button-modifier.html)』提到的用法。




## Alt-Tab Switcher


## Window / Previous

> 執行下面指令，綁定「`Win + a`」來切換聚焦到「`上一個視窗`」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings switch-windows-backward "['<Super>a']"
```




## Window / Next

> 執行下面指令，綁定「`Win + s`」來切換聚焦到「`下一個視窗`」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings switch-windows "['<Super>s']"
```




## Workspace / Previous

> 執行下面指令，綁定「`Alt + a`」來切換到「`上一個工作空間`」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-left "['<Alt>a', '<Alt>Left']"
```




## Workspace / Next

> 執行下面指令，綁定「`Alt + s`」來切換到「`下一個工作空間`」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-right "['<Alt>s', '<Alt>Right']"
```


| 方位        | 按鍵           | 功能                    |
| ----------- | -------------- | ----------------------- |
| 左 (Left)   | `Win + a`      | `Window / Previous`     |
| 右 (Right)  | `Win + s`      | `Window / Next`         |
| 左 (Left)   | `Alt + a`      | `Workspace / Previous`  |
| 右 (Right)  | `Alt + s`      | `Workspace / Next`      |

> 關於「grave」指是「`」，在「Tab鍵」上方的那個「鍵盤按鍵」。

> `Win` for `Window`

> `Alt` for `Workspace`




## Window / Tiling Move

> 設定參考指令如下

``` sh

##
## ## Window / Tiling Move
##

gsettings set org.gnome.desktop.wm.keybindings maximize "['<Control><Super>Up']"

gsettings set org.gnome.desktop.wm.keybindings unmaximize "['<Control><Super>Down']"

gsettings set org.gnome.mutter.keybindings toggle-tiled-left "['<Control><Super>Left']"

gsettings set org.gnome.mutter.keybindings toggle-tiled-right "['<Control><Super>Right']"

```


## Screenshot

> 執行下面指令，探索關於「`screenshot`」的「按鍵綁定」設定

``` sh
gsettings list-recursively | grep screenshot | grep budgie
```

顯示

```
com.solus-project.budgie-wm full-screenshot-cmd ''
com.solus-project.budgie-wm take-full-screenshot ['Print']
com.solus-project.budgie-wm take-region-screenshot ['<Ctrl>Print']
com.solus-project.budgie-wm take-region-screenshot-cmd ''
com.solus-project.budgie-wm take-window-screenshot ['<Alt>Print']
com.solus-project.budgie-wm take-window-screenshot-cmd ''
org.buddiesofbudgie.budgie-desktop.screenshot delay 0
org.buddiesofbudgie.budgie-desktop.screenshot file-type 'png'
org.buddiesofbudgie.budgie-desktop.screenshot include-cursor false
org.buddiesofbudgie.budgie-desktop.screenshot include-frame true
org.buddiesofbudgie.budgie-desktop.screenshot last-save-directory 4
org.buddiesofbudgie.budgie-desktop.screenshot screenshot-capture-sound true
org.buddiesofbudgie.budgie-desktop.screenshot screenshot-mode 'Screen'
org.buddiesofbudgie.budgie-desktop.screenshot showtooltips true
```


> 執行下面指令，修改關於「`screenshot`」的「按鍵綁定」設定

``` sh

##
## ## Screenshot
##

gsettings set com.solus-project.budgie-wm take-full-screenshot "['Print']"


##
## ## Screenshot / Window
##

gsettings set com.solus-project.budgie-wm take-window-screenshot "['<Super>Print']"


##
## ## Screenshot / Area
##

gsettings set com.solus-project.budgie-wm take-region-screenshot "['<Ctrl>Print']"

```

> `Super` for `Window`

> `Control` for `Area`




## 統整

> 統整以上提到的綁定

``` sh

##
## ## Fix
##


##
## ## Application / Launcher
##

gsettings set org.gnome.desktop.wm.keybindings panel-main-menu "['<Alt>F1']"

gsettings set org.gnome.desktop.wm.keybindings panel-run-dialog "['<Alt>F2']"


##
## ## Window
##

gsettings set org.gnome.desktop.wm.keybindings close "['<Super>q']"

gsettings set org.gnome.desktop.wm.keybindings toggle-maximized "['<Super>w']"

gsettings set org.gnome.desktop.wm.keybindings toggle-fullscreen "['<Super>f']"

gsettings set org.gnome.desktop.wm.keybindings show-desktop "['<Super>d']"

gsettings set org.gnome.desktop.wm.keybindings begin-move "['<Super>e']"

gsettings set org.gnome.desktop.wm.keybindings begin-resize "['<Super>r']"


##
## ## Window / Switch
##

gsettings set org.gnome.desktop.wm.keybindings switch-windows-backward "['<Super>a']"

gsettings set org.gnome.desktop.wm.keybindings switch-windows "['<Super>s']"

gsettings set org.gnome.desktop.wm.keybindings cycle-windows-backward "['<Alt>Escape', '<Super>Left']"

gsettings set org.gnome.desktop.wm.keybindings cycle-windows "['<Super>Escape', '<Super>Right']"


##
## ## Workspace / Switch
##

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-up "[]"

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-down "[]"

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-left "['<Alt>a', '<Alt>Left']"

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-right "['<Alt>s', '<Alt>Right']"

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-last "['<Alt>z']"


##
## ## Overview / Switch
##

## > None Overview


##
## ## Window / Tiling Move
##

gsettings set org.gnome.desktop.wm.keybindings maximize "['<Control><Super>Up']"

gsettings set org.gnome.desktop.wm.keybindings unmaximize "['<Control><Super>Down']"

gsettings set org.gnome.mutter.keybindings toggle-tiled-left "['<Control><Super>Left']"

gsettings set org.gnome.mutter.keybindings toggle-tiled-right "['<Control><Super>Right']"


##
## ## Screenshot
##

gsettings set com.solus-project.budgie-wm take-full-screenshot "['Print']"


##
## ## Screenshot / Window
##

gsettings set com.solus-project.budgie-wm take-window-screenshot "['<Super>Print']"


##
## ## Screenshot / Area
##

gsettings set com.solus-project.budgie-wm take-region-screenshot "['<Ctrl>Print']"

```


> 另外關於「Workspace」，我會做如下的額外設定


``` sh

gsettings set org.gnome.desktop.wm.preferences num-workspaces 5

gsettings set org.gnome.desktop.wm.preferences workspace-names "['File', 'Edit', 'Web', 'Term', 'Misc']"




gsettings set org.gnome.mutter dynamic-workspaces false

```




## 範例腳本

* [範例腳本](https://github.com/samwhelp/note-about-ubuntu-budgie/tree/gh-pages/_demo/scripts/budgie-keybind)
