---
layout: default
title: Mini Debian Conference Japan 2016 Key sign party
organizer: Mini Debian Conference Japan 2016 実行委員会
event_date: 2016-12-10 JST
event_datetime: 2016-12-10 (土) 10:00-18:00 JST
event_party_time: aa:aa-bb:bb
---
<a name="outline"></a>

## キーサインパーティ開催概要
   
Mini Debian Conference Japan 2016 にて PGP/GPG
キーサインパーティを行います。
キーサインパーティーとは、互いの鍵に署名をすべく、PGP/GPG 鍵を持つ人々が集まるものです。 
キーサインパーティーは PGP/GPG 鍵を利用する上で非常に重要な概念である、
信頼の輪 ([Web of Trust](http://en.wikipedia.org/wiki/Web_of_trust))を 大規模に拡張するのに有用です。 
また、このようなキーサインパーティーは実際に開発者と面と向かって会う良い機会でもあります。

- 開催日時・会場
  - 日時: 2016年12月10日 (時間はまだ未定です。当日スケジュールと同時にアナウンスされます。)
  - 会場: [サイボウズ株式会社](http://cybozu.co.jp/company/info/)
          東京都中央区日本橋2-7-1 東京日本橋タワー
  - キーサインコーディネイター: 岩松 信洋 / iwamatsu at debian.org

## 内容

今回のキーサインパーティは、一斉に事務的に行うのではなく、 相手と軽く会話をしながらお互いのIDとPGP/GPG フィンガープリントを確認するという方法で行います。
（通常のキーサインパーティでは、参加者は印刷物に記載された番号の順に2列に並び、 対面相手のIDを確認し、その後に左に1歩ずれて次の人に、という方法を採ります。）

今回のキーサインパーティーには、[Debian Project](http://www.debian.org)、[Linux Kernel](http://kernel.org)などのフリーソフトウェア開発者の参加も予定されています。
フリーソフトウェアの世界では、ネット上で自分の存在を保証してもらうために、PGP/GPG を使ったWeb of Trust を構築しています。
フリーソフトウェアの開発に参加している方、参加を考えている方はこれを機会に参加してみてはいかがでしょうか。

## 参加方法と注意事項

参加希望者は2016年12月4日
(日) 23時59分 までに、 キーサインに使用する自分の公開鍵を
[登録サイト](https://docs.google.com/forms/d/e/1FAIpQLSeqltqvI2mNk_ukjH9hms6b4buEJnszCrjPPxvDr1Q7yjiJkg/viewform)から登録してください。
公開鍵を登録前に <span style="text-decoration: underline;">~/.gnupg/gpg.conf</span> に以下の内容があるか、確認してください。

<pre>
digest-algo sha256
personal-digest-preferences SHA256
cert-digest-algo SHA256
default-preference-list SHA512 SHA384 SHA256 SHA224 AES256 AES192 AES CAST5 ZLIB BZIP2 ZIP Uncompressed
</pre>

また、公開鍵は以下の方法でクリアサインしたものを登録してください。

<pre>
$ gpg --armor --export-options export-clean,export-minimal --export &quot;自身の鍵ID&quot; | gpg --local-user &quot;自身の鍵ID&quot; --clearsign
</pre>

鍵の登録後、登録データに問題が無ければコーディネーターが[参加者の一覧](ack-list.html)に登録します。 
このリストに乗った時点で登録完了とします。
なお、登録作業から24時間経過しても、コーディネーターからの連絡も無く、 かつ参加者の一覧にも掲載が無い方は、コーディネーターまでご連絡ください。
また今回のキーサインパーティーでは、より強い
暗号を持ったPGP/ GPG鍵に限定します。
昔からPGP/GPGを利用されている方は、まだ1024/DSAをお使いだと思います。2048/RSA以上鍵を作成し、その鍵を利用してキーサインパーティーに参加してください。
コーディネータがあなたの鍵を確認したら、確認メッセージをメールで送信します。 もし、メッセージに書かれている情報が間違っている場合、すぐにご連絡ください。
正常に受け付けられた鍵と参加者の一覧については [確認用参加者の一覧ページ](ack-list.html)をそちらを確認してください。

## Q and A

### キーサインとはなんですか? なぜ必要なのですか?

キーサインパーティーは、互いの鍵に署名をすべく、PGP/GPG鍵を持つ人々が集まるものです。 キーサインパーティーはWeb of Trustを大規模に拡張するのに寄与します。

### キーサインはどのように行いますか?

パーティーは「Len Sassaman の効果的なグループキーサイン方式」を使って進めます。 これは、皆さんが知っているやり方よりもいくぶん早くキーサインできる手順です。

### 登録用データの作成方法はどうすればよいですか？

[参加登録用ウェブページ](https://docs.google.com/forms/d/e/1FAIpQLSeqltqvI2mNk_ukjH9hms6b4buEJnszCrjPPxvDr1Q7yjiJkg/viewform) から登録する PGP/GPG 鍵の情報については、

<pre>
gpg --armor --export-options export-clean,export-minimal --export &quot;自身の鍵ID&quot; | gpg --local-user &quot;自身の鍵ID&quot; --clearsign
</pre>

というAscii形式で出力したものをそのまま貼り付けてください。
[サンプル](signed-gpg-key-sample.html) のようなものが出力されているはずです。

コマンドラインが使えない環境の方は、別途コーディネイタにご相談ください。

### 当日の飛び込み参加できます？

飛び込み参加は基本的には <strong><em>推奨しません</em></strong> 。参加希望者は <strong><em>2016年12月4日 (日) 23時59分</em></strong> までに登録を完了してください。
どうしても参加したい方は、名前、鍵、メールアドレス、 フィンガープリントが書かれた紙を用意して参加してください。
なおこの紙は、キーサインパーティーで確認をする際に相手に1枚ずつ配っていただきますので、それなりの数をご用意ください。作成方法は [キーサイン用データの作り方](https://sites.google.com/site/kspjapanese/create-keysign-data) を参照してください。
<hr>

## 登録後の当日までの流れ

### 事前配布物の確認

2016年12月4日(日) 23時59分 の締め切り後、翌日朝までに
<a href="miniconf2016-ksp.txt">鍵一覧用ファイル</a> (<a href="miniconf2016-ksp.txt.sha256">鍵一覧用ファイルハッシュ値</a>, <a href="miniconf2016-ksp.txt.sha256.asc">コーディネイターによる署名ファイル</a>)
がアップロードされます。
鍵一覧用ファイルにあるあなたの鍵のフィンガープリントが正しいかどうか照合してください。
さらに、ファイルの SHA256 ハッシュ値を計算してください。 たとえば sha256sum コマンドを使って次のように求められます。

<pre>
$ sha256sum miniconf2016-ksp.txt
</pre>

または、gpg のコマンドでも確認することができます。

<pre>
$ gpg --print-md sha256 miniconf2016-ksp.txt
</pre>

一覧用ファイルを印刷して、計算したハッシュ値を書き込んでください。 当日は、このハッシュ値を書き込んだ紙が必要となります。

### 当日の流れ

- 本キーサインパーティはDebian miniconfのPGP/GPG キーサインパーティで行ないます。
- 当日、コーディネーターが用意したスライドに SHA256 ハッシュ値が表示されます。 このハッシュ値とあなたの計算したものが合致していることを確認します。 これで、全参加者が同じ鍵リストに基いての参加であることを保証できます。
- 会場で皆さんが集合したところで、コーディネーターがファイルのSHA256ハッシュ値が、 全員同じであることを尋ね、全参加者が同じリストを持っていることを確認します。 この確認の際に、印刷物の各ページに照合した旨のチェックをつけておいてください。
- この後、確認された人にキーサイン用のネームタグを配布します。
- 次のステップは、各参加者の同一性保証です。 参加者の免許書・パスポート等による ID 書類によって確認します。 この確認は、懇親会を含めたイベント中に随時行っていただけます。

<strong><em>注意事項:ネームタグを持っている人のみとPGP/GPG鍵交換することができます。 ネームタグを持っていない人のハッシュ値は間違っている可能性があるからです。</em></strong>

- イベント後、 鍵の持ち主の確認とフィンガープリントが印刷物のどのフィンガープリントに合うというチェックが付いていれば、 ID確認済みの鍵です。PGP/ GPG鍵にサインした後、その鍵の所有者に送ります。

### 当日何を持ってくるべきか

- 一覧用ファイルの印刷物。印刷物にあるあなたの名前、フィンガープリントおよびメールアドレスが正しいことを確認してください。
- 一覧用の SHA256 ハッシュ値。これで、全員が同じ印刷物を持っていることを保証できます。
- 政府発行の何らかの ID - パスポートや運転免許証など。
- 鉛筆、あるいはボールペン
- あなたにとってこれが最初のキーサインであれば、このサイトを印刷したものや、[GnuPG README 日本語訳](http://www.hyuki.com/gnu/gnupg-v12-readme.html)も役に立つでしょう。

## GnuPG鍵の作り方

- [GnuPG鍵の作り方](https://sites.google.com/site/kspjapanese/create-gpgkey) を参考にしてください。4096R の鍵の作り方になっています。</li>
- 既に GnuPG 鍵を持っており、4096/RSA に更新したい人は [4096/RSA 鍵 の追加方法](https://sites.google.com/site/kspjapanese/create-gpgkey-4096r) を参照してください。

## お問い合わせ

何か不明な点があれば、iwamatsu _at_ debian.org までお気軽にお問い合わせください。
