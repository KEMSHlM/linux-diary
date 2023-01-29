# Ubuntu Linux setting
## 最初に
ubuntuのバグがでた際に，再インストールが最も簡単な改善方法である．  
そのたびに設定を繰り返すことになるので，ここに加えた方法を明記しておく．  
- キーボード設定  
    標準搭載ではないfcitxの利用が良さそうだ．crtl+spaceで日本語と英語の切り替えができる．しかし，xmodでctrl+hjklと併用はできないみたいだ．  

- neovim  
    前から次の環境はneovimにしようと心に決めていた．  
    - [インストール手順](https://zenn.dev/temple_c_tech/articles/upgrade-nvim)  
    - [拡張機能管理ツール](https://github.com/Shougo/dein-installer.vim)  

- zsh  
    - [oh-my-zsh](https://qiita.com/NaokiIshimura/items/249bb1a101b626a59387)  

- samba  
    以下が参考にしたサイト． しかし，簡易的な設定のみ組み込んだ．後々設定を書き換えていこう．  
    - [ubuntuでファイルサーバー構築](https://www.pc-koubou.jp/magazine/10062)  
    - [sambaでの詳しめの設定](https://seesaawiki.jp/w/bokkuri_orz/d/CentOS%20-%20samba)  
    以下にIPアドレスの固定方法の参考文献である．  
    - [IPアドレスの固定方法](https://gihyo.jp/admin/serial/01/ubuntu-recipe/0708)  
    以下にMACでの接続方法を乗せる． 共有フォルダ自体にシンボリックリンクを貼ることはできないのかもしれない．  
    - [MACでファイルサーバーに接続する方法](https://pc-karuma.net/mac-mount-windows-share-folder/)  