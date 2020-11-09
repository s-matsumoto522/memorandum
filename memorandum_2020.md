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

## Github
### 便利なコマンド
* 戻したいとき
    * https://qiita.com/rch1223/items/9377446c3d010d91399b

## Markdown
* VscodeのMarkdownをPDFに変換する時に数式をちゃんと表示させる方法
    * https://qiita.com/1gy/items/5b1f3c772b6da43cc13e

## ssh接続
* 接続が切れるまでの制限時間を延ばしたい
    * ~/.ssh/configの時間を延ばしたいHostのところに次を追記．<br>ServerAliveInterval 60
