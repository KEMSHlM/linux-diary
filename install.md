# linux settings
## 1. install   
インストールには，苦労した．  
手順については，詳しく [Ubuntuインストール手順](https://blog.kabocy.com/linux/6550/)に記載されてある．
OSのisoイメージをusbかCDに焼いて，起動してあげる必要がある．今回はCDを利用した．~~usbはうまく行かなかった．~~   

最初に[月間Linux](https://info.nikkeibp.co.jp/media/LIN/atcl/mag/120100066/)の付録インストールCDからのインストールを試みた．  
付録されているバージョンは，21.10であった．初回のインストールは難なく成功し，苦労はなかった．  
その後，RTX4090に対応したBIOSに更新するため，[gigabyteのホームページ](https://www.gigabyte.com/jp/Motherboard/B650-AERO-G-rev-10#kf)より当時最新のBIOSであるf4hを導入することにした．  
- BIOS 更新  
    bios画面よりGUIをもちいて，BIOSを更新した．しかし，その後ubuntuが起動しなくなった．  
    f4hのインストール方法を間違えたみたいだ．正しいインストール手順は最新BIOSをダウンロードした際に入ってある手順に従ってダウンロードする必要があった．  
    - 手順
        1. biosをusbに入れる．
        2. AEROの画面でdelキーを押し，BIOS画面を開く．
        3. 起動順番を切り替えて，bootのCSMを切り替え，再起動．
        4. gurubメニューが立ち上がるので，FS1: からの flash.nshを実行．

だが，Ubuntuが起動しないではないか．再インストールもできなかった．そこで，BIOSをf4c → f3へと変更した．  
再インストールはできるが，前にインストールしたOSは起動できないままだ．  
- OSのインストール   
    最初に，USBによるインストールを試みた．しかし，なぜかうまくいかない．  
    埒が明かないので，家電量販店でCDとCD読み書き装置を購入し，isoイメージをCDに書き込んでインストールすることにした．  
    せっかくなので，最新の22.10のインストールを行うことにした．  
    OSを焼くのには，macを利用した．焼くのは簡単でisoイメージを右クリックのメニューから選択できる．  
    全然インストールがうまくいかない．CDで起動したUbuntuが以上に遅い．  
    対策は，[Ubuntu日本語フォーラム / 22.04LTS 日本語Remix ライブＤＶＤ 動作報告](https://forums.ubuntulinux.jp/viewtopic.php?pid=124569)に載っていたので，  
    これに従ってインストールを進めた．また，インストールは稀に成功する(笑)．  

## 2. Error
インストール手順は上で確立した．しかし，インストール後にubunutuがおかしくなる．  
その度，再インストールを繰り返した．以下のエラー現象が起きた．  
- grubメニューが表示される  
    インストール後にソフトをダウンロードしていたら，grubメニューに飛ばされて解決策を調べたがどれもうまくいかなかった．  
    OSを再インストールしたあとに従って[grub解決策](https://ocucraqp.hatenablog.com/entry/2020/04/26/114439)を読みながら再発防止に成功している．   
- インターネット接続がなくなる  
    この現象もいきなり陥った．ethやwifiのファームウェアの対応ができてないことが原因？  
    ネットの文献を読む限りこの現象に陥るまでに  
    ```bash
        sudo apt install build-essential
        sudo apt install net-tools    
    ```
    はやっておかないと詰む．  
    いまのところ，OS再インストールでごまかしている．
       
