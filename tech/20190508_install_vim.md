# vimのインストール

Macに最初入っていたvimをそのまま使っていたのでgitを使うようにした。

ref. https://www.vim.org/git.php

## 最初のインストール
```
$ git clone https://github.com/vim/vim.git
$ cd vim
$ cd src
$ make
$ sudo make install
```

.zshrcに以下の設定を追加する。
元々のvimが/usr/binにあり、上記でinstallしたvimが/usr/local/binにあるのでそちらを見るための設定。
```
export PATH=/usr/local/bin:$PATH
```

ちゃんと設定できているか確認
```
$ which vim
/usr/local/bin/vim
$ vim --version
VIM - Vi IMproved 8.1 (2018 May 18, compiled May  8 2019 15:08:17)
macOS version
Included patches: 1-1295
<略>
```

## 更新
```
$ cd vim
$ git pull
$ cd src
$ make distclean
$ make
$ sudo make install
```
