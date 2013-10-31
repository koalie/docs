{{Page_Title|リンクの貼り方}}
{{Flags
|State=Unreviewed
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|この文書では、HTMLのアンカーの基本的な取り扱い方を提供します。すなわち、<a> 要素についてで、一般的にはHTMLのリンクとして知られています。}}
{{Guide
|Content={{Languages}}

== はじめに ==

このドキュメントでは、Webの歴史上で画期的な発明の1つである「リンク」について学んでいきます。ドキュメントの読者は、瞬時にドキュメントからドキュメント、サーバーからサーバーへとジャンプできます。リンクが初めて導入されてから色々なことが起こりましたが、1つだけ変わらないことがあります。それは、リンクはwebでの出来事において極めて重要な要素であるということです。そして、webサイトの訪問者がコンテンツを簡単に利用できるか否かは、リンクをいかに使用するのかにかかっています。

この文書では、理解がやさしく、どんな環境でも機能するリンクの作り方を調べます。さらに、リンクが検索エンジンでの評判にどう影響するのかを見てから、リンクのテキストの言い回しについてのちょっとした情報に触れます。

== リンクとは?==

''リンク'' は、別のリソース— 他のHTMLドキュメントやテキストファイル、PDFファイル等 —を指すHTMLドキュメントの一部です。中にはブラウザが自動的に生じさせるものもあり、これは <code>&lt;link&gt;</code> 要素を使って作られます(既に以前の文書で目にしています。その時はCSSファイルを読み込み、HTMLドキュメントに入れ込むのに使っていました)。しかし一般的にリンクを話題にしている時は、ページの著者によって作られ、ユーザーが選ぶか否かを決めるものを指します。これらは ''アンカー'' と呼ばれ、<code>&lt;a&gt;</code> 要素を使ってHTMLドキュメントに入れます。

== アンカーを分析する ==

どんなインライン要素やテキストでも、<code>&lt;a&gt;</code> 要素で囲むことによってHTMLのリンクにできます。例えば、下記のHTMLドキュメントでは「Opera Software」がリンクです。

<syntaxhighlight lang="html5"><!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Link Example</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>A link to Opera</h1>
  <p><a href="http://www.opera.com">Opera Software</a></p>
</body>
</html></syntaxhighlight>

このリンクを選択した訪問者は(マウスでクリックするかキーボードで選択するか、場合によっては音声で)、今いるページを離れてOperaのホームページに行きます。さらにリンク自身に起こる変化があります。これについては、リンクのデザインを話題にする時に検討しましょう。

アンカータグには、追加できる属性がいくつかあります。

* <code>href</code> — リンクが指すリソース(外部ファイルやアンカーID)
* <code>id</code> — リンクの一意の識別名で、CSSでリンクを整形する場合やJavaScriptで参照する場合に役立つ。 <code>id</code> 属性は、リンクをページのアンカーにするのにも使え、 別の <code>&lt;a&gt;</code> 要素からリンクするのにも使える
* <code>class</code> — リンクにCSSのクラス名を適用する。例えば、ページ上の特定のリンクだけを整形したい場合に役に立つ
* <code>title</code> — ブラウザがマウスを重ねた時、表示すべきリンクに関する追加情報

== href 属性 ==

<code>&lt;a&gt;</code> 要素には複数の役目があり、どの属性を設定するによって決まります。みなさんが最も使うであろう一般的な属性は、 <code>href</code> 属性です。これはリンクが指すリソースが何であるかを定義します。この属性には様々な値を入れられます。

* 現在のフォルダーに対する相対URL。例えば、「../../help/help.html」(2つのドットの意味は「サイトのフォルダー階層を1レベル上がる」)。もしくは、サーバーのルートに対する絶対URL。例えば、「/help/help.html」(URLの先頭にある前部のスラッシュは、フォルダー階層のルートからアドレスが始まることを意味する)
* 別のサーバのURL。例えば、<nowiki>"ftp://ftp.opera.com/"</nowiki> や <nowiki>"http://developer.yahoo.com/yui"</nowiki>
* フラグメント識別子もしくはハッシュ記号で始まるid。例えば、「#menu」。これは外部URLというよりも現在のドキュメント内部の対象を指す
* URLとフラグメント識別子の組み合わせ。つまり、URLにフラグメント識別子を続けて <code>href</code> 属性を指すことで、異なるドキュメントのセクションに直接リンクできる。例えば、 <nowiki>"http://dev.opera.com/articles/view/new-structural-elements-in-html5/#aside"</nowiki>

== id属性でページ内のナビゲーションを作る ==

<code>&lt;a&gt;</code> 要素に <code>id</code> 属性を付けることで、ページのアンカーにできます。ページのアンカーは、そのページにある他のリンクのためのページ内部の ''対象(target)'' です。別のリンクの <code>href</code> 属性にあるIDを入れることで、リンクできます。例えば、下記はリンク対象になるようにコーディングされたアンカーです。

<syntaxhighlight lang="html5"><h2><a id="sec1">Section #1</a></h2></syntaxhighlight>

この対象は、下記のリンク表現でリンクされます。

<syntaxhighlight lang="html5"><a href="#sec1">Section One</a></syntaxhighlight>

都合が良いことに、最近のたいていのブラウザは、これを「省略した表現」で書けます。下記のように、リンクしたい要素に直接IDを指定できます。

<syntaxhighlight lang="html5"><h2 id="sec1">Section #1</h2></syntaxhighlight>

これはさらにシンプルなので、可能な限りこうすることをお勧めします。

下記のHTMLには、様々なタイプのリンクがあります。

<syntaxhighlight lang="html5"><!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Different Links Example</title>
  <link rel="stylesheet" href="linkexamplestyles.css">
</head>
<body>
  <h1>Different Links</h1>

  <h2>Example of in-page navigation with fragment identifiers, links, and anchors</h2>
  <div id="nav">
    <ul id="toc">  <!--Table of Contents-->
      <li><a href="#sec1">Section One</a></li>
      <li><a href="#sec2">Section Two</a></li>
      <li><a href="#sec3">Section Three</a></li>
      <li><a href="#sec4">Section Four</a></li>
      <li><a href="#sec5">Section Five</a></li>
    </ul>
  </div>

  <div id="content">
    <div>
      <h2 id="sec1">Section #1</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
    <div>
      <h2 id="sec2">Section #2</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
    <div>
      <h2 id="sec3">Section #3</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
    <div>
      <h2 id="sec4">Section #4</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
    <div>
      <h2 id="sec5">Section #5</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
  </div>

  <h2>Some other link examples</h2>

  <ul>
    <li><a href="http://dev.opera.com">Opera Developer Network</a></p></li>
    <li><a href="http://www.wait-till-i.com/stuff/JavaScript-DOM-Cheatsheet.pdf">Dom Cheatsheet</a></p></li>
    <li><a href="ftp://get.opera.com/pub/opera/win/">Download different Opera versions</a></li>
    <li><a href="http://farm1.static.flickr.com/56/188791635_0b8bdd808d.jpg?v=0">Photo of my book</a></li>
  </ul>

  </body>
</html></syntaxhighlight>

このファイルをお気に入りのブラウザで開いて、試してみてください。最初のリストのどのリンクを選択しても、同じページの正しいセクションにジャンプするのが分かると思います。また、ブラウザのロケーションバーにあるURLが変更されているのにも、気付かれるかもしれません。URLの最後の所にフラグメント識別子が表示されていますが、これは訪問者がこのセクションをブックマークできること、他の人々にリンクを電子メールで送り、行くべき所を誤りなく伝えられることを意味します。要点をまとめると、

* アンカーのリンクは、<code>href</code> 属性の値として、フラグメント識別子を持てる。このフラグメント識別子は、ハッシュ記号(#)で始めなければならない
* 選択した時、そのリンクはこの値の <code>id</code> が付いたどんなHTML要素へもジャンプする。すべてのIDは、ページ内では一意でなければならない
* IDには名前付けのルールがある。最も肝心なのは、アルファベット文字で始めなければいけないこと、スペースを入れてはいけないこと

このまとめが取り上げているのは、上記の例にあるメニューと様々なセクションです。しかし他のリンクはどうでしょう? 試してみれば、他の対象を指しているのが分かるでしょう—あるものは他のサイトへ、もう１つは写真を、3番目は他のwebページの特定のセクションを表示します(特定のIDにジャンプするのが分かります)。すべてが上手く動けば上出来です—しかしもしブラウザが判断できないリソースがあったら、どうなるでしょうか?

== リンクしているものについて、曖昧なままにしておいてはいけない ==

リンクについて覚えておかなければならない重要なことは、リンクが訪問者とみなさんとを結びつける、実質的な要素であるということです。読者は皆さんが用意したリンクを信じて、それをたどって関連が高い情報を取得できます。もしリンクされたリソースが利用できなかったり、訪問者のブラウザでは使えないフォーマットであったり、といった理由でリンクが機能しなければ、信頼を裏切ることになり、信用を失います。そうさせてはいけません。

=== title属性を使って追加情報を提供する ===

他のHTML要素の大部分と同じく、<code>&lt;a&gt;</code> 要素に <code>title</code> 属性を加え、追加情報を入れられます。
訪問者がマウスカーソルをリンクに重ねた時に、ブラウザは ''ツールチップ'' を表示します。一般的にツールチップは、訪問者にリンクが何についてなのかを伝えます。例えば、内容について少し紹介したり、リンクされたドキュメントの場所を伝えたりします。

<syntaxhighlight lang="html5"><!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
<title>Adding extra information with a title attribute</title>
<link rel="stylesheet" href="linkexamplestyles.css">
</head>
<body>
  <h1>Adding extra information with a title attribute</h1>
  <ul>
    <li>Find more information on the <a title="The Yahoo Developer Network is the hub for Yahoo's developer tools"
     href="http://developer.yahoo.com">Yahoo Developer Network</a>.</li>
  </ul>
</body>
</html>
</syntaxhighlight>

しかし、極めて重要な情報のために <code>title</code> 属性をよりどころにするほど、訪問者が辛抱強く、目と手が連携するだろうと当てにはできません。
視覚的な障害があるユーザーはページがよく見えず(もしくはまったく見えないかも)、この情報に十中八九たどり着けません。スクリーンリーダーには <code>title</code> 属性を読み込めるユーザー用のオプションがありますが、この機能は普通デフォルトでは無効になっています。これがリンクでとても重要な情報を <code>title</code> 属性で決して使うべきではない理由です。

極めて重要な情報は、下記のようかもしれません。

* PDFファイルや動画、音声ファイルといったHTMLではないリソースにリンク。もしくはダウンロード対象
* 現在のサイトを離れて、別のサーバーにリンク(外部リンク)
* 違うフレームやポップアップで開くドキュメントにリンク

=== HTMLではないリソースへのリンク—人に推測させるな ===

リンクをクリックした時、ブラウザがリンクが指すコンテンツをどう扱ってよいのか判断できないと、とても不愉快になるでしょう。残念なことにあまりに多くのwebサイトが、訪問者が望むことを伝えることなく、画像やPDFドキュメント、動画をリンクしているのを見かけます。
さらに言えば、リソースが極端に大きく、訪問者がブラウザ内で開くよりもダウンロードしたくなることもあるかもしれませんし、まったく利用したくないかもしれません。

webページが最も成功を収める要因の１つは、ユーザーがある行為をした時に、何が起こるのか推測させないことです。その代わりに、ユーザーにその行為が何をもたらすのかを直接教えます。リンクされたリソースの場合、必要なのは訪問者にどんなリソースがリンクされているのか教えることだけです。
例をいくつかあげます。

<syntaxhighlight lang="html5"><!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
<title>Linking non-HTML resources</title>
<link rel="stylesheet" href="linkexamplestyles.css">
</head>
<body>
  <h1>Linking non-HTML resources</h1>

  <ul>
    <li>Find more information on the <a href="http://developer.yahoo.com">Yahoo
      Developer Network site (external)</a></li>
    <li>Download the <a href="http://www.wait-till-i.com/stuff/JavaScript-DOM-Cheatsheet.pdf">
      Dom Cheatsheet (PDF, 85KB)</a></li>
    <li>Pick and <a href="ftp://get.opera.com/pub/opera/win/">download different Opera
      versions from their FTP (external)</a></li>
    <li>Check out a <a href="http://farm1.static.flickr.com/56/188791635_0b8bdd808d.jpg?v=0">
      Photo of my book (JPG, 200KB)</a></li>
  </ul>

</body>
</html></syntaxhighlight>

リンクされたファイルとその種類についての情報を用意することで、それをどう扱うのかを訪問者に委ねます。訪問者のブラウザの設定やプレインストールしたソフトウェアを当てにするよりも。そのような情報を巧みに配置することで、リンクを魅力的で直感的に理解できるものにすることさえできます。例えば、複数のタイプのリンクに簡単に見分けがつくアイコンを用意するとか(これについての詳細は、 [[guides/Styling lists and links]] )。慎重さを求めるなら、種々のファイルフォーマットが何で、表示に必要なソフトウェアがどこで得られるかを説明したヘルプセクションを用意してもよいでしょう。

== 外部リンク vs 内部リンク ==

商用webサイトが一番恐れていることの1つは、人々が早々にサイトを去ってしまうことです。これがよく起こる原因は、サイトが第三者のリンクを用意していないことです(お金を受け取って、第三者向けのwebトラフィックを特別扱いしていなければ)。この判断ミスについては、再び取り上げます。ここでは、訪問者がうっかりサイトから去ってしまわないように、開発者ができることについて少し話します。そして、この対策がどうやってサイトを成功させるかについても話します。

=== フレームとポップアップ — まったく駄目! ===

他のサイトへのリンクを望んでいながら他のサイトへ訪問者をとられる恐怖から、私たちはweb開発において何年もユーザビリティで苦労の元となっている2つの革新技術(?)を取り入れました。

HTMLのフレームを使うということは、ブラウザが表示するページを様々な異なるドキュメントに分割することになります。これの長所は、違うコンテンツをロードした時にそれが自身のサーバーからであっても第三者のサーバーからであっても、一見同じ状態のままなことです。ただ、役に立つのもここまでです。簡単に言うと、フレームはユーザーにとても不快な思いをさせます。例えば、サイトがフレームを使っていると下記のようになります。

* 検索エンジンがページ全体をインデックスできない。検索した結果は、文脈を無視した意味のないページの一部だけが表示される
* 訪問者が見た状態のページをブックマークできない。ブックマークを後で開くと、フレームセットの初期状態を見ることになり、以前訪れたページを見られない
* 支援技術に頼っている訪問者は、フレームセット間を行き来するのにかなり苦労する
* 第三者はフレームセット内で自分のサイトが表示されるのを望まないかもしれない。そのため「framebreaker」スクリプトを使って、組み込もうとした時に本当のURLにフレームセットを置き換える。これは、インターネットユーザーに本物に似せたwebサイトへ個人情報を入力させるよう誘導する犯罪(フィッシング)を止めるのにも使われている

フレームセット内のリンクは、正しいフレームを対象にするため、アンカーの <code>target</code> 属性を使します。フレームセット内のそれぞれのフレームは一意の名前になり、選択したリンクはフレーム内の <code>href</code> 属性で設定されたドキュメントを開きます。フレームセットが利用できないと(例えば、訪問者が検索エンジン経由でリンクのドキュメントを見つけた場合)、ブラウザが新規インスタンスでリンクを開きます。

新規インスタンスでブラウザを開くのは、第三者のサイトへリンクするよくやる方法の1つで、スクリプトでウィンドウをポップアップするか、<code>target</code> 属性に <code>_blank</code> という値を設定するかします。最近のブラウザはポップアップをブロックするようになっていることから、現在このやり方がいかに人気がないかが分かるでしょう!

要するに、 '''<code>target</code> 属性は、自分が何をしているのか理解していない限り、リンクを作るときには使用するな''' ということです。もはやそれは古くなった知識で、事実上すべてのブラウザはタブ化したインターフェースを持ち、簡単にユーザーは皆さんのサイトを離れることなく、第三者のサイトを違うタブで開けます。特定の状況のもとでは、外部と内部のリンクの違いを示したい場合があるかもしれませんが、それをどう扱うかは常に訪問者に委ねてください。

=== 外部へのリンクと内部へのリンクのメリット ===

第三者のサイトが競争相手であっても、リンクするもっともな理由があります。

* 訪問者には信頼性があると映る。コンテンツの品質に自信があるので、競争相手を避けていないと思われる
* 包括的なサービスを提供する良い機会である。自分のサイトでは取り上げていないが、今関心があるテーマを掘り下げたい訪問者が、興味を持つかもしれない他のサイトの内容と文書もしくは製品を提供できる
* 第三者による先に書かれた文書を基にしたり、リンク経由で古い文書を参照することで、より改良された解決方法や違う視点の解決策を提供したりすることで、自分の正しさを証明できる

内部へのリンク(第三者からみなさんのサイトを指すリンク)の有用さは、あまり議論されていません。そうなのですが、質の高いサイトからあなたのサイトへのリンクがあればあるほど、検索エンジンのランクがさらに高くなります。しかしそうなる前には、他のサイトへのリンクを尻込みしないこともはっきりと示さなければいけません。

優れたリンクを張るには、もう1つとても重要なことがあります。それは、リンクをどうやって言葉で表すか、です。

== リンクの言い回し(ワーディング) ==

「HTMLではないリソースへのリンク」についてのセクションでこの件を簡単に説明しましたが、リンクは対話型の要素であるだけではなく、ページの材料として欠かせない一部である、と自分に言い聞かせましょう。

支援技術には、訪問者がすみやかにナビゲーションができて希望のリンクが見つかるように、ドキュメント全体を示すのではなく、リンクの一覧を用意するものがあります。これはリンクのテキストが文脈に沿う沿わないに依存せずに意味を持つ必要がある、ということです。このことは、Operaで簡単にチェックできます。webサイトを開いて、メニューから <code>Tools &gt; Links</code> もしくは <code>Ctrl + Shift + L</code> してください。新しいタブが開いて、リンクが指すドキュメントとリソースをすべて表示するでしょう。 <ref> 訳注：現在のOpera(Opera 31.0)はこの機能を実装していません。拡張機能もない? ようです。なお、Firefoxの拡張機能である [https://addons.mozilla.org/ja/firefox/addon/linksidebar/?src=dp-dl-oftenusedwith LinkSidebar] を使うと、webページ内のリンクの一覧が見られます。 </ref>

同じ言い回しで異なるリソースを指しているリンクが複数ないことも確かめてください。典型的な間違いに「ここをクリック」的なリンクがあります。「ツールの最新版をダウンロードするには、<u>ここをクリック</u> 」のようなものです。それよりも、リンクが何を指すのかを説明するリンクのテキストを使う方が好ましいでしょう。例えば、その文を「 <u>ツールの最新版をダウンロード</u>できます。試してみてください。」に変えます。

同じことが、「もっと・さらに」的なリンクにも当てはまります。このリンクはニュースサイトでよく見られ、見出しやティーザー広告のテキストに続けて「もっと読む」や「全部読む」といったリンクがあります。この問題に対する解決策は、代わりとなる一意のテキストが付いた「もっと」画像リンクを使うか、「もっと」の後のリンク内に <code>&lt;span&gt;</code> 要素を追加し、CSSで隠すようにします。

== リンクのデザイン ==

リンクのデザインすべてを扱うと、この文書の範疇を超えてしまいます(詳しい情報は、 [[guides/Styling lists and links]] にあります)。それでも、リンクがどのように見えるのかを知っておくこと、そして検討すべきリンクの様々な状態があることを覚えておくことは大切です。リンクの状態(CSSの ''疑似クラスセレクター'' と言います)は次の通りです。

* <code>:link</code> (デフォルト) — 普通は訪問していないリンクの体裁を明示。デフォルトでは訪問していないリンクは、青
* <code>:visited</code> — 既にクリックした(訪問した)リンクの体裁を明示。デフォルトでは訪問したリンクは、紫
* <code>:hover</code> —マウスカーソルが重なった時のリンクの体裁を明示
* <code>:focus</code> — マウスでクリックもしくはキーボードのような別の制御機構によってフォーカス(ハイライトされる)した時のリンクの体裁を明示。
* <code>:active</code> — 選択された状態のリンクの体裁を明示。つまり、対象への接続が継続している状態。ブラウザの戻る機能を使ってドキュメントにたどり着いた時に、最後に選択したリンクの体裁でもある

== HTML5のブロックレベルのリンク ==

HTML4では、<code>&lt;a&gt;</code> 要素が他のインライン要素をリンクに変えることを禁止していました。ほとんどの場合はこれでかまいませんでした。しかし、例えば複数の画像と段落がある広告バナーのセクションを丸々リンクにしたい時は面倒でした。コードを正しくしておくためには、個々のちょっとしたテキストと画像をそれぞれ別個のリンクで囲まなければいけませんでした &mdash;  同じようなところすべてでです &mdash;  これは恐ろしいほどの繰り返し作業になるだけでなく、支援技術とその利用者に混乱をもたらします。インライン要素でブロックレベルの内容のセクションを囲んでも、デザインが妙なことになります。CSSを使ってブロックレベルの要素であるかのごとく表示するよう設定しない限りは。

幸いなことに、HTML5はこの制限を無くしました。これで希望するコンテンツがいくらあっても1つのリンクで囲むことができます。きちんと動かすには、ブロックレベル要素のようにリンクが動作しなければいけません。しかしこれは簡単で、以前に比べてはるかに融通が利くようになりました。例を見てみましょう。

<syntaxhighlight lang="html5"><!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Block level link Example</title>
  <link rel="stylesheet" href="styles.css">
  <style>
    a {
      display: block;
      background-color: blue;
      text-decoration: none;
      color: white;
      width: 300px;
      height: 100px;
    }

    a:hover {
      background-color: red;
    }

  </style>
</head>
<body>
  <a href="http://www.opera.com">
    <h1>A link to Opera</h1>
    <p>Opera Software</p>
  </a>
</body>
</html></syntaxhighlight>

これを見ると、<code>&lt;a&gt;</code> 要素が見出しと段落を囲んでいるのが分かると思います。うまく動作させるには、CSSで <code>display: block;</code> を設定する必要があります。ご自分で試してみれば、ブロック全体がクリックできるリンク領域になっているのが分かるでしょう。見やすくするため、マウスが重なった時にbackground-colorが変わるように設定を追加しています。

== 結論 ==

この文書でたくさんのことを説明しました。しかし多分この文書から持ち帰ることで一番肝心なのは、リンクが何をするかだけでなく、リンクは何を '''すべき''' か、を忘れないということです。
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections==== 練習問題 ===

* 次のリンクは何が誤っているか? <code>&lt;a href="report.pdf" title="report as PDF, 2.3MB"&gt;get our latest report&lt;/a&gt;</code>
* リンク内の <code>target</code> 属性は、何のためにあるのか? またそれを使うと何か良いことがあるのか?
* リンクの関連性とリンクとアンカー間の関係を説明してきた。ドキュメント間の関連性を表すリンク用の属性も存在するか?
* 訪問者がクリックした時にページを読み進める要素に導くリンクをどのように書けるのか? あらかじめ何を確認する必要があるのか?
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
}}