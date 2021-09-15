# Setting

## ubuntuキーボード設定

* **Mozc でキーボードの配列が日本語にならないのを解決する** [**https://qiita.com/arai-wa/items/3123ecb350097f79c6ef**](https://qiita.com/arai-wa/items/3123ecb350097f79c6ef)\*\*\*\*
* Ubuntu18.04にて、USキーボードを用いて英数字と日本語\(ひらがな\)の切り替えを行う方法 [https://magidropack.hatenablog.com/entry/2019/01/05/174048](https://magidropack.hatenablog.com/entry/2019/01/05/174048)
* [https://golang.hateblo.jp/entry/ubuntu-keyboard-layout](https://golang.hateblo.jp/entry/ubuntu-keyboard-layout)

```text
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

```text
$ sudo vim /usr/share/ibus/component/mozc.xml

<layout>ja</layout>
```



