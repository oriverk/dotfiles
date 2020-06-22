## first
this `.vimrc` bases on the post by ryuta66 [vimって極めればvscode並のIDEになるんじゃないの？](https://qiita.com/ryuta69/items/98901f4c4f0683e7aa57)

## install
1. install `.vimrc` on top directory
2. then type following command

```sh
cd ~/
vim +PlugInstall +qall
cd .vim/plugged/YouCompleteMe/
/usr/bin/python2.7 ./install.py --all
```

## usage
* **Space + dir** ⇛　カレントディレクトリのファイルが左に開く。

選択してEnterでファイルが開きます。
選択してTでファイルが別タブに開きます。

* **Space + sh** ⇛　カレントディレクトリのターミナルが右側に開く。

ここでプログラムを実際に実行したり、grepしたりgitできます。
grep, gitなどのプラグインもありますが、コマンドを覚えるのが面倒です。
ターミナルを開いた方が楽！

* **Space + go** ⇛　vimで開いているファイルを実行して、下画面にログを出す。

C言語やPythonなど、ファイルを開きながらプログラムを実行できちゃうのです。
プログラミングコンテストなどで必須。

* **コメントアウトしたい行をマウスでもビジュアルでも複数選択して、 gcc**

自動コメントアウトしてくれます

* **文章を綺麗に整えたい複数文章を選択して、 ga（整列したい文字）**

```python:test.py
a = 2 + 5
aaaa = 2 + 5
aaa = 2 + 5

# ⇑の３行を選択して、ga=と押すと下のように整理される。
a    = 2 + 5
aaaa = 2 + 5
aaa  = 2 + 5
```

* **適当にファイルを開いて、 ./ と書いてみる**

ディレクトリの補完が効いてます

* **適当にファイルを開いて、普通にプログラムを書いたり、変数を入力**

プログラム命令の補完、変数の補完が効いてます

* **Space + w** ⇛ セーブ。:wと同じです。　

* **Space + qqq** ⇛ 強制終了。:q!と同じです。

* **Space + wq** ⇛ セーブ終了。:wqと同じです。

* **Space + t** ⇛ タブを開く。:tabnewと同じです

* **Shift + y** ⇛　文末までの行をコピー

* **+** ⇛　数字の上でやると、数字が増えていきます。

* **-** ⇛　数字の上でやると、数字が減っていきます。

* **tab(エスケープコードで)** ⇛　１５文字ずつ右に移動します。

* **Shift + tab(エスケープコードで)** ⇛　１５文字ずつ左に移動します。

* **emacs/bash風移動**

Ctl + e ⇛　文末まで移動
Ctl + a ⇛　文頭まで移動
Ctl + f ⇛　一文字後に移動
Ctl + b ⇛　一文字前に移動

## WSLなどでエラーを吐く場合
10/8追記　@htnabe さん情報
おそらくyoucompletemeプラグインの関係で正常動作しない可能性があります。
その際は下記記事を参考に、.vimrcでycm serverのパスをpython2.7からpython3.〇のようにpythonのバージョンに合わせてください。
https://qiita.com/TsutomuNakamura/items/2fc8aa6c0feaf31c86e4


## 自分にあったテーマを探す
まずvimのテーマは２種類存在します。
以下が、世に出ている全てのテーマが一覧されているサイトです。
### ターミナル自体のテーマ
https://github.com/lysyi3m/macos-terminal-themes
### Vim自体のテーマ
https://vimcolors.com/

ちなみに私は、sublimeやatomでも有名な[ayu](https://github.com/dempfi/ayu)というのを使っています。
<img width="808" alt="スクリーンショット 2019-04-07 23.14.57.png" src="https://qiita-image-store.s3.amazonaws.com/0/257108/dc4b8853-4805-9542-bd3c-25042cd2739a.png">

## まとめ 「vimは最高なんだ・・・vimは最高なんだ・・・」
vimって操作覚えるのも一苦労だと思うんです。
でも、**全ての環境で動くのはvimだけ**なんです

