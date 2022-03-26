# Setting

## ubuntuキーボード設定

```
sudo apt-get install ibus-mozc  
```

* **Mozc でキーボードの配列が日本語にならないのを解決する**\
  ****[**https://qiita.com/arai-wa/items/3123ecb350097f79c6ef**](https://qiita.com/arai-wa/items/3123ecb350097f79c6ef)****
* Ubuntu18.04にて、USキーボードを用いて英数字と日本語(ひらがな)の切り替えを行う方法\
  [https://magidropack.hatenablog.com/entry/2019/01/05/174048](https://magidropack.hatenablog.com/entry/2019/01/05/174048)
* [https://golang.hateblo.jp/entry/ubuntu-keyboard-layout](https://golang.hateblo.jp/entry/ubuntu-keyboard-layout)
* [https://johnyuan2000.hatenablog.com/entry/2020/07/06/163112](https://johnyuan2000.hatenablog.com/entry/2020/07/06/163112)

```
$ sudo dpkg-reconfigure keyboard-configuration


Keyboard model:

  Generic 105-key (Intl) PC


Country of origin for the keyboard:

  Japanese


Keyboard layout:

  Japanese


Key to function as AltGr:

  The default for the keyboard layout


Compose Key:

  No compose key


Use Control+Alt+Backspace to terminate the X server?

  <No>
```

```
$ sudo vim /usr/share/ibus/component/mozc.xml

<layout>ja</layout>
```

### Kali usキーボード ctrl+spaceで入力切替

[https://cocolofun.co.jp/linux-upgrade/](https://cocolofun.co.jp/linux-upgrade/)

![](.gitbook/assets/ibus\_setting.png)

![](.gitbook/assets/ctrl\_space\_setting.png)

## conda promptの(BASE)消す

```
$ conda config --set changeps1 False
```

## install sublime-text

```
sudo apt-get upgrade
```

```
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
sudo apt-get install apt-transport-https
echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
sudo apt-get update
sudo apt-get install sublime-text
```

## zsh\_prompt

```
PROMPT="%F{047}┌[%f%F{cyan}%m%f%F{047}]─[%f%F{255}%D{%H:%M-%d/%m}%f%F{047}]─[%f%F{magenta}%d%f%F{047}]%f"$'\n'"%F{047}└╼%f%F{green}$USER%f%F{yellow}$%f"
```
