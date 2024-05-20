---
title: 設定 Application Appearance
nav_order: 7023
has_children: false
parent: 如何
---


# 設定 Application Appearance


## 執行指令

``` sh

gsettings set org.gnome.desktop.interface gtk-theme 'Arc-Dark'

gsettings set org.gnome.desktop.interface icon-theme 'Papirus-Dark'

gsettings set org.gnome.desktop.interface cursor-theme 'breeze_cursors'

```


## 圖形使用者介面操作

可以在「桌面」按下「滑鼠右鍵」，會出現一個選單，

選項如下：

* Budgig Desktop Settings
* System Settings

選擇「Budgig Desktop Settings」，就會出現一個「設定程式」。

也就是透過「budgie-desktop-settings」這個「圖形使用者介面程式」來操作

``` sh
budgie-desktop-settings
```

> 執行「`grep '^Exec=' /usr/share/applications/org.buddiesofbudgie.BudgieDesktopSettings.desktop`」可以找到上面的指令。
