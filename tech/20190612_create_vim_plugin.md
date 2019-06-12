# Vimプラグインの作り方

`~/.vim/pack/myplugin/start/myplugin`を作り、以下のようにファイルを置く。
すると起動時に読み込んでくれる。

```
.
├── README.md
├── autoload
│   └── myplugin.vim
└── plugin
    └── myplugin.vim
```

[Vim 8 時代のがんばらないプラグイン管理のすすめ](http://tyru.hatenablog.com/entry/2017/12/20/035142)
