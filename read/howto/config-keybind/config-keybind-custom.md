---
title: 設定「自訂」的「按鍵綁定」
nav_order: 7020
has_children: false
parent: 設定「按鍵綁定 (Keybind)」
grand_parent: 如何
---


# 設定「自訂」的「按鍵綁定」




## 主題

* [前提](#前提)
* [設定範例](#設定範例)




## 前提




## 設定範例

``` sh

##
## ## Clear Old
##

dconf reset -f /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/




##
## ## Keybind Item
##


## ### Logout
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-logout/name "'System_Logout'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-logout/command "'budgie-session-quit --logout'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-logout/binding "'<Shift><Alt>x'"


## ### Shutdown
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-shutdown/name "'System_Shutdown'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-shutdown/command "'budgie-session-quit --power-off'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-shutdown/binding "'<Shift><Alt>z'"


## ### System Settings
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/control-center/name "'Control_Center'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/control-center/command "'budgie-control-center'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/control-center/binding "'<Shift><Alt>s'"


## ### Terminal
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal/name "'Terminal'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal/command "'xfce4-terminal'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal/binding "'<Alt>Return'"


## ### Terminal-1
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal-1/name "'Terminal-1'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal-1/command "'xfce4-terminal'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal-1/binding "'<Shift><Alt>a'"


## ### File Manager
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager/name "'File_Manager'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager/command "'nemo'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager/binding "'<Shift><Alt>f'"


## ### File Manager 1
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager-1/name "'File_Manager-1'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager-1/command "'thunar'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager-1/binding "'<Shift><Alt>g'"


## ### Text Editor
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/text-editor/name "'Text_Editor'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/text-editor/command "'gedit'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/text-editor/binding "'<Shift><Alt>e'"


## ### Web Browser
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/web-browser/name "'Web_Browser'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/web-browser/command "'firefox --new-tab about:blank'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/web-browser/binding "'<Shift><Alt>b'"




##
## ## Custom Keybindings
##

gsettings set org.gnome.settings-daemon.plugins.media-keys custom-keybindings "['/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-logout/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-shutdown/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/control-center/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal-1/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/text-editor/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/web-browser/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager-1/']"

```

> 上面設定完後，就會綁定成功。

> 可以執行下面指令，觀看目前的設定值。

``` sh

dconf dump /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/

echo

gsettings get org.gnome.settings-daemon.plugins.media-keys custom-keybindings

```

顯示

```

```
