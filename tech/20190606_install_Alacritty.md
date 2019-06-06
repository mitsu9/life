# Install Alacritty

[Alacritty](https://github.com/jwilm/alacritty)を導入することにしたのでそのメモ.

乗り換えた理由は、
- 設定をファイルで管理できる
- どのOSでも使える
- tmuxを覚えたかった(iTerm2だとそちらでいろいろできてしまう)

## Install
もしrustがなければここから
```
$ curl https://sh.rustup.rs -sSf | sh
// .zshrcに以下を追加
$ export PATH=$HOME/.cargo/env:$PATH
```

```
$ ghq get https://github.com/jwilm/alacritty.git
$ cd .ghq/github.com/jwilm/alacritty
$ make app
$ cp -r target/release/osx/Alacritty.app /Applications/
```

## setting

WIP
