# B4のための備忘録
忘れがちなことをみんなで共有しましょう！

## 使用上の注意
* 書き込む前にgit pull origin master
* 書き込んだ後はgit push origin master
* このファイルはmarkdownの書式を使っています. コマンドは下のチートシートを参照してね. 
    * https://qiita.com/Qiita/items/c686397e4a0f4f11683d
* 下に一例を挙げておきます. あくまで参考程度にどうぞ
## 数学
### コーシー・リーマンの関係
$f(z) = u(x, y) + iv(x, y)$が点$z$で微分可能, すなわち正則であれば, $u, ~v$が全微分可能であり, 以下の関係が成り立つ.
$$u_{x} = v_{y},~~~v_{x} = -u_{y}$$
これを**コーシー・リーマンの関係**という. これは逆も成り立つ. （編集: 松元）（追記：江口）

## 材料力学

## Fortran
* ディレクトリ作成方法．次の記事の3つ目のサブルーチンをコピペ．
    * https://qiita.com/aisha/items/c41c09b0587ba6503733
* コンパイラをgfortranからifortに変えると速くなる．次の記事を参考にIntelのコンパイラ（ifort）をインストールした．（岩下）
    * Ubuntu 20.04には未対応．（2020年9月現在）
    * https://qiita.com/minwinmin/items/afbb0404533fd4b07e72 
    * 研究室サーバーにはインストールされている．

## ターミナル
### コマンド
* コマンド履歴から検索して実行．（`Ctrl`+`R`）
    * `Ctrl`+`R`をしてから，検索したいコマンドを入力すると最新の履歴が表示される．`Enter`で実行，`→`または`←`でコマンドを編集できる．
    * あるいは，検索したいコマンドを入力してから`Ctrl`+`R`を押していくとコマンド履歴を遡れる．
    * https://qiita.com/quwa/items/3a23c9dbe510e3e0f58e
### Terminator
* 分割できたりするので便利．インストールは`sudo apt install terminator`．
* Ubuntuの場合，`Ctrl`+`Alt`+`T`で起動する．デフォルトのターミナルからは`terminator`で起動できる．
* ショートカットキー一覧
    * https://qiita.com/genchi-jin/items/cf7b81d8d9ecdb69b64a
    * 上の記事にないもの．
        * 左のタブ`Ctrl`+`Page Up`
        * 右のタブ`Ctrl`+`Page Down`
### Windows Terminal
* Windowsの場合はWindows Terminalの方が相性がいいかもしれない．（Terminatorも一応使えるがたまに不具合があったりした．）
    * Microsoft Storeからインストールできる．

## Github
### 便利なコマンド
* 戻したいとき．
    * https://qiita.com/rch1223/items/9377446c3d010d91399b

## Markdown
* VScodeのMarkdownをPDFに変換する時に数式をちゃんと表示させる方法．
    * https://qiita.com/1gy/items/5b1f3c772b6da43cc13e
* WindowsでMarkdownをpdf化したときに数式がうまく変換されないとき
    * http://yamaken.tokyo/2019/03/17/post-97/  
    この「数式を使う」の章を参考にして、.mdファイル内に呪文を書き込む。

## ssh接続
* 接続が切れるまでの制限時間を延ばしたい．
    * ~/.ssh/configの時間を延ばしたいHostのところに次を追記．<br>ServerAliveInterval 60
* パスフレーズを省略したいとき．
    * 「ssh-add [秘密鍵のパス]」が便利．
        https://qiita.com/Yarimizu14/items/6a4bab703d67ea766ddc

## Vim
* コマンドまとめ
    * https://qiita.com/hide/items/5bfe5b322872c61a6896
    * https://qiita.com/ktoyod/items/0a8491cdb6c0191ab0cc
* Vimのカラースキームを変える．
    * デフォルトのカラー（特に青）は見づらいので，カラースキームをmolokaiにするのが簡単なのでおすすめ．
    * http://pyoonn.hatenablog.com/entry/2014/10/04/225321
## 研究室サーバー
* 使用量確認コマンド
    * 各領域の使用量確認→`df -h`  
        https://www.atmarkit.co.jp/ait/articles/1610/24/news017.html
    * 自分の使用量確認→`du -hs`  
        https://webkaru.net/linux/du-command/
* 連番ファイルを一括で削除する方法（例えば, 標準出力ファイルやエラーファイル）
    * `rm -rf hoge.o{12345..97654}`（中カッコ内の数字は連番の最初と最後に合わせる）

## Slack
* テキストメッセージの編集コマンド
    * Markdownとほとんど同じ．<br>
        `code block` （`で囲む）
        
        ```
        code （```で行を挟む）
        ```
        >quotation （>に続けて入力）
        
        _italic_ （_で囲む）  
        **bold** （*で囲む）  
        ~~strike~~ （~で囲む）  
* Slack小技集  
        https://businesschatmaster.com/slack/advanced_skill_slack#Markdown

## Ubuntu
* コピー・移動・リンク作成
    * `Alt`を押しながらドラッグ&ドロップで選択肢が表示される．

## $\LaTeX$（卒論）
* bibをうまく呼び出せない時
    * 中間ファイルを全て消去した後, コンパイルしなおすとうまくいくかも
* 全角括弧の位置が変な時
    * `sudo kanji-config-updmap-sys ipaex`
* 論文執筆にあたり, 知っておくべきこと
    * https://qiita.com/birdwatcher/items/5ec42b35d84d3ee2ffbb

## リモート間のデータ転送
ローカルを経由せずにリモート間のデータ転送を行う方法
`scp -3`コマンドを用いる

* 例: 後藤研サーバーの`hoge`に東大の`fuga`というディレクトリを転送したい場合（どちらのディレクトリもホームにあると仮定）
    * `scp -r -3 ofp.jcahpc.jp:fuga 192.168.1.11:~hoge`



## Python

### カラーマップの構成色を自作する方法

- もっとうまいやり方はありそうやけど、とりあえず以下のように書けばできました。<br/>

  ```
  import matplotlib.colors as mcolors
  
  cm = mcolors.LinearSegmentedColormap.from_list('name', ['blue', 'white', 'gold'])
  ```

  色を指定する配列は16進数でも大丈夫みたいです。あとは、実際にカラーマップを作成するときに<br/>

  ```
  cmap = cm
  ```

  としておくだけです。

