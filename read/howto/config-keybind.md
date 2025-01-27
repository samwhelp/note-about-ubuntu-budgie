---
title: 設定「按鍵綁定 (Keybind)」
nav_order: 7030
has_children: true
parent: 如何
---


# 設定「按鍵綁定 (Keybind)」




## 主題

* [前提](#前提)
* [設定方式](#設定方式)
* [相關議題](#相關議題)




## 前提

> 執行下面指令，探索關於「`keybind`」的設定。

``` sh
gsettings list-recursively | grep 'keybind'
```

> 有很多行，就不列在此佔篇幅




> 執行下面指令，探索關於「`org.gnome.desktop.wm.keybindings`」的設定。

``` sh
gsettings list-recursively | grep org.gnome.desktop.wm.keybindings
```

顯示

```
org.gnome.desktop.wm.keybindings activate-window-menu ['<Alt>space']
org.gnome.desktop.wm.keybindings always-on-top @as []
org.gnome.desktop.wm.keybindings begin-move ['<Alt>F7']
org.gnome.desktop.wm.keybindings begin-resize ['<Alt>F8']
org.gnome.desktop.wm.keybindings close ['<Alt>F4']
org.gnome.desktop.wm.keybindings cycle-group ['<Alt>F6']
org.gnome.desktop.wm.keybindings cycle-group-backward ['<Shift><Alt>F6']
org.gnome.desktop.wm.keybindings cycle-panels ['<Control><Alt>Escape']
org.gnome.desktop.wm.keybindings cycle-panels-backward ['<Shift><Control><Alt>Escape']
org.gnome.desktop.wm.keybindings cycle-windows ['<Alt>Escape']
org.gnome.desktop.wm.keybindings cycle-windows-backward ['<Shift><Alt>Escape']
org.gnome.desktop.wm.keybindings lower @as []
org.gnome.desktop.wm.keybindings maximize ['<Super>Up']
org.gnome.desktop.wm.keybindings maximize-horizontally @as []
org.gnome.desktop.wm.keybindings maximize-vertically @as []
org.gnome.desktop.wm.keybindings minimize ['<Super>h']
org.gnome.desktop.wm.keybindings move-to-center @as []
org.gnome.desktop.wm.keybindings move-to-corner-ne @as []
org.gnome.desktop.wm.keybindings move-to-corner-nw @as []
org.gnome.desktop.wm.keybindings move-to-corner-se @as []
org.gnome.desktop.wm.keybindings move-to-corner-sw @as []
org.gnome.desktop.wm.keybindings move-to-monitor-down ['<Super><Shift>Down']
org.gnome.desktop.wm.keybindings move-to-monitor-left ['<Super><Shift>Left']
org.gnome.desktop.wm.keybindings move-to-monitor-right ['<Super><Shift>Right']
org.gnome.desktop.wm.keybindings move-to-monitor-up ['<Super><Shift>Up']
org.gnome.desktop.wm.keybindings move-to-side-e @as []
org.gnome.desktop.wm.keybindings move-to-side-n @as []
org.gnome.desktop.wm.keybindings move-to-side-s @as []
org.gnome.desktop.wm.keybindings move-to-side-w @as []
org.gnome.desktop.wm.keybindings move-to-workspace-1 ['<Super><Shift>Home']
org.gnome.desktop.wm.keybindings move-to-workspace-10 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-11 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-12 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-2 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-3 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-4 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-5 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-6 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-7 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-8 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-9 @as []
org.gnome.desktop.wm.keybindings move-to-workspace-down ['<Control><Shift><Alt>Down']
org.gnome.desktop.wm.keybindings move-to-workspace-last ['<Super><Shift>End']
org.gnome.desktop.wm.keybindings move-to-workspace-left ['<Super><Shift>Page_Up', '<Super><Shift><Alt>Left', '<Control><Shift><Alt>Left']
org.gnome.desktop.wm.keybindings move-to-workspace-right ['<Super><Shift>Page_Down', '<Super><Shift><Alt>Right', '<Control><Shift><Alt>Right']
org.gnome.desktop.wm.keybindings move-to-workspace-up ['<Control><Shift><Alt>Up']
org.gnome.desktop.wm.keybindings panel-main-menu ['<Alt>F1']
org.gnome.desktop.wm.keybindings panel-run-dialog ['<Alt>F2']
org.gnome.desktop.wm.keybindings raise @as []
org.gnome.desktop.wm.keybindings raise-or-lower @as []
org.gnome.desktop.wm.keybindings set-spew-mark @as []
org.gnome.desktop.wm.keybindings show-desktop ['']
org.gnome.desktop.wm.keybindings switch-applications ['<Super>Tab', '<Alt>Tab']
org.gnome.desktop.wm.keybindings switch-applications-backward ['<Shift><Super>Tab', '<Shift><Alt>Tab']
org.gnome.desktop.wm.keybindings switch-group ['<Super>Above_Tab', '<Alt>Above_Tab']
org.gnome.desktop.wm.keybindings switch-group-backward ['<Shift><Super>Above_Tab', '<Shift><Alt>Above_Tab']
org.gnome.desktop.wm.keybindings switch-input-source ['<Alt>Shift_L', '<Super>space', 'XF86Keyboard']
org.gnome.desktop.wm.keybindings switch-input-source-backward ['<Super><Shift>space', '<Shift>XF86Keyboard']
org.gnome.desktop.wm.keybindings switch-panels ['<Control><Alt>Tab']
org.gnome.desktop.wm.keybindings switch-panels-backward ['<Shift><Control><Alt>Tab']
org.gnome.desktop.wm.keybindings switch-to-workspace-1 ['<Super>Home']
org.gnome.desktop.wm.keybindings switch-to-workspace-10 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-11 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-12 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-2 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-3 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-4 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-5 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-6 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-7 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-8 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-9 @as []
org.gnome.desktop.wm.keybindings switch-to-workspace-down ['<Control><Alt>Down']
org.gnome.desktop.wm.keybindings switch-to-workspace-last ['<Super>End']
org.gnome.desktop.wm.keybindings switch-to-workspace-left ['<Super>Page_Up', '<Control><Alt>Left']
org.gnome.desktop.wm.keybindings switch-to-workspace-right ['<Super>Page_Down', '<Control><Alt>Right']
org.gnome.desktop.wm.keybindings switch-to-workspace-up ['<Control><Alt>Up']
org.gnome.desktop.wm.keybindings switch-windows @as []
org.gnome.desktop.wm.keybindings switch-windows-backward @as []
org.gnome.desktop.wm.keybindings toggle-above @as []
org.gnome.desktop.wm.keybindings toggle-fullscreen @as []
org.gnome.desktop.wm.keybindings toggle-maximized ['<Alt>F10']
org.gnome.desktop.wm.keybindings toggle-on-all-workspaces @as []
org.gnome.desktop.wm.keybindings unmaximize ['<Super>Down', '<Alt>F5']
```




> 執行下面指令，探索關於「`org.gnome.mutter.keybindings`」的設定。

``` sh
gsettings list-recursively | grep org.gnome.mutter.keybindings
```

顯示

```
org.gnome.mutter.keybindings cancel-input-capture ['<Super><Shift>Escape']
org.gnome.mutter.keybindings rotate-monitor ['XF86RotateWindows']
org.gnome.mutter.keybindings switch-monitor ['<Super>p', 'XF86Display']
org.gnome.mutter.keybindings toggle-tiled-left ['<Super>Left']
org.gnome.mutter.keybindings toggle-tiled-right ['<Super>Right']
```




## 設定方式

> 接著我們在『[設定「主要」的「按鍵綁定」](https://samwhelp.github.io/note-about-ubuntu-budgie/read/howto/config-keybind/config-keybind-main.html)』這篇來說明如何修改設定。




## 相關議題

* [設定「主要」的「按鍵綁定」](https://samwhelp.github.io/note-about-ubuntu-budgie/read/howto/config-keybind/config-keybind-main.html)
* [設定「自訂」的「按鍵綁定」](https://samwhelp.github.io/note-about-ubuntu-budgie/read/howto/config-keybind/config-keybind-custom.html)
