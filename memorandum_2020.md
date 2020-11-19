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
    * https://qiita.com/minwinmin/items/afbb0404533fd4b07e72 

## Github
### 便利なコマンド
* 戻したいとき．
    * https://qiita.com/rch1223/items/9377446c3d010d91399b

## Markdown
* VscodeのMarkdownをPDFに変換する時に数式をちゃんと表示させる方法．
    * https://qiita.com/1gy/items/5b1f3c772b6da43cc13e

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
* 連番ファイルを一括で削除する方法(例えば, 標準出力ファイルやエラーファイル)
    * `rm -rf hoge.o{12345..97654}`(中カッコ内の数字は連番の最初と最後に合わせる)

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
