思う事だが。9.x系まで、alma rocky使ったが、

CISA High
suloginを読み込ませない必要あり
＊ArchISO等からrootをマウント　mv　sbin/sulogin 〜/sbin/sulogin.bak

Q.じゃあその後のアップデートは？dnf-3 updateで、サブコマンドが権限付与許可ないから、出来ない！
A.ひとまずSElinux等からも許可を得ているソフトウェアアプリを使わざる得ないかと。。

手順☟
sudo dnf-update → 許可がありません。とエラー停止確認。→ ソフトウェアアプリ起動。　そのままアップデートタブより更新(こちらの更新には、触れない、ややこしくなる)

以上

DISA 
普段使いは、むしろこっちなのか？？
PAMモジュールによるログイン監視が厳しいの良いが。
連続して4文字が英単語と認識された時点でどんなにランダムだろうが20文字だろうが、弾かれて相当苦労したのを覚えてる。
(…こいつ…特殊文字で区切らないとアルファベットな時点で弾いてる希ガス)


話を戻ると　NSAが管理してるCISAのhighプロファイル。　sudoについても詳しく制限されていて、結構面白い。
(数ヶ月前までenhanceが最上位だと思ってたが、Highが最上位。)

詳しくは、redhatブログ及び　openscap_redhat9(8) cisaプロファイル参照

＊almaは、9早く出したくせにcisa highプロファイルにて、最新でなかったのは、どういう訳か
(Rockyでも何故か8.6で最新だったが… バージョン再び下がってる)
→下がってるというかusrの分離も最新では、当たり前なんだが。
分離しなくともコンプライアンスを潜り抜ける為に。。
んーこの。。

…issuesにも、minimalでは、コンプライアンスが正常に起動しないとは、あるが…DVDイメージやぞ…

