

<h1 style="line-height:1.4;font-size:2em">CSSレイアウトテクニック</h1>

----

# 今日話すこと

<ol style="font-size:1.1em;">
<li>インラインレベル要素とブロックレベル要素</li>
<li>各種プロパティに関して</li>
<li>ブロックの拡張性</li>
<li>余白の設計</li>
</ol>

----

<p style="font-size:1.6em;">インラインレベル要素とは</p>

<p style="font-size:1.2em; text-align: left">行の流れを分断することなく、テキスト行に要素ボックスを生成する。<br>
a、span、em、strong、imgなどがインラインレベル要素。<br>
これらの要素は要素ボックスの前後に改行を生成しない。したがって別の要素のコンテンツで囲むようにしても、表示が分断されることはない。
</p>

* [inline sample](http://jsdo.it/kotaro_tan/sr1Ba)

----

<p style="font-size:1.6em;">ブロックレベル要素とは</p>

<p style="font-size:1.2em; text-align: left">簡単にいうと一つの独立したまとまり。<br>
p、div、h1〜h6などがブロックレベル要素。<br>
ブロックレベル要素は要素ボックスの前後に改行を発生する。
</p>

* [block sample](http://jsdo.it/kotaro_tan/tlJl)

----

<p style="font-size:1.6em;">text-align</p>

<p style="font-size:1.2em; text-align: left">このプロパティは、要素のテキスト行を互いに整列させる。</p>

* [text-align sample](http://jsdo.it/kotaro_tan/mTlb)

----

<p style="font-size:1.6em;">float</p>

<p style="font-size:1.2em; text-align: left">floatプロパティはボックスを左、もしくは右に寄せて配置させるためのプロパティ。<br>flotプロパティを指定したボックスの、後に続くボックスは、floatプロパティを指定したボックスが無いものと仮定して配置され、その内容領域だけが重なりを避けるように回り込んで行く。</p>

* [float sample](http://jsdo.it/kotaro_tan/2GXt)

----

<p style="font-size:1.6em;">floatを使う時の注意点</p>

* [カラム落ち](http://jsdo.it/kotaro_tan/r1Er)
* [マージンの相殺](http://jsdo.it/kotaro_tan/ll9M)
* [floatを解除する手法](http://jsdo.it/kotaro_tan/uSkw)

----

<p style="font-size:1.6em;">position</p>

<p style="font-size:1.2em; text-align: left">positionプロパティは、ボックスの表示位置を決める配置方法を指定するためのプロパティで。指定できる値は親要素を継承するinheritを除くと、static、relative、absolute、fixedの4種類がある。</p>

----

<p style="font-size:1.6em;">static</p>

<p style="font-size:1.2em; text-align: left">この値を指定したボックスは、通常の配置方法にしたがって配置されます。つまりpやdivといったブロックレベル要素の場合は最上部から、垂直方向に徐々に配置され、spanやaといったインラインレベル要素のボックスの場合、親ボックスから水平方向に徐々に配置される。特にpositionプロパティに何もしていしないときはstaticが初期値として選択される。</p>

----

<p style="font-size:1.6em;">relative</p>

<p style="font-size:1.2em; text-align: left">この値を指定したボックスは、staticと同様に、通常の配置方法にしたがって配置されます。この時、left、topといったプロパティを併用することで、ボックスを通常配置位置から相対的にずらして配置することができる。後に続くボックスはrelativeを指定したボックスが通常の配置位置にあると仮定して配置されていく。</p>

* [relative sample](http://jsdo.it/kotaro_tan/x2Di)

----

<p style="font-size:1.6em;">absolute</p>

<p style="font-size:1.2em; text-align: left">absoluteを指定したボックスの配置位置は親ボックスのうちでもっとも近い層のボックスを基点とします。
absoluteを指定したボックスの親ボックスとなるのはstatic以外の値が指定されているボックスです。もし親ボックスがない場合はウインドウ領域を配置の基点とします。
absoluteで指定したボックスは、通常配置とは独立して扱われ他のボックスの配置に影響を与えなくなります。</p>

* [absolute sample](http://jsdo.it/kotaro_tan/4cL8i)

----

<p style="font-size:1.6em;">display:inline-block</p>

<p style="font-size:1.2em; text-align: left">
displayにinline-blockが指定された要素は、中にブロックレベルの要素を入れることができるブロックコンテナですが、要素の外からは、img要素のようなインラインレベル要素として扱われる、インラインブロックになります</p>

* [inline-block sample](http://jsdo.it/kotaro_tan/uo8t)

----

<p style="font-size:1.4em;">ちょっとvertical-alignの話</p>

<p style="font-size:1.2em; text-align: left">
vertical-alignプロパティは、行のなかでのテキストや画像などの縦方向の揃え位置を指定する際に使用します。
vertical-alignプロパティを適用できるのは、インライン要素とテーブルセルです。ブロックレベル要素には適用できません
</p>

* [line-height:smaple](http://jsdo.it/kotaro_tan/dhKL)
* [vertical-align:sample](http://jsdo.it/kotaro_tan/3ql7)

----

<p style="font-size:1.6em;">inline-blockを使ったレイアウト</p>

* [inline-block sample](http://jsdo.it/kotaro_tan/hBlx)

----

<p style="font-size:1.6em;">display:table</p>

<p style="font-size:1.2em; text-align: center">
<img style="vertical-align: middle;" src="https://fbcdn-sphotos-g-a.akamaihd.net/hphotos-ak-xap1/v/t1.0-9/943791_540967899299840_2055971151_n.jpg?oh=2c9ec665a2fdb9ad9062b0e3c7ad06c8&oe=55917E36&__gda__=1435597749_0801e360280afcaf7fed8048c89849b4">「display:tableは甘え」
</p>

----

<p style="font-size:1.2em; text-align: left">とは言うものの<br>
すごく便利なので積極的に使いましょう！<br>
ただしIE6、7に対応しなければならない案件では注意です。</p>

----

<p style="font-size:1.6em;">改めてdisplay:table</p>

<p style="font-size:1em; text-align: left">
table<br>
tableに相当する。テーブルボックスの起点になれる。ブロックレベルでレイアウトされる。paddingは適用できない。</p>
<p style="font-size:1em; text-align: left">
table-cell<br>
thとtdに相当する。包含するボックスに対するvertical-alignが有効。marginは適用できない。</p>

* [display:table sample](http://jsdo.it/kotaro_tan/qy7B)

----

<p style="font-size:1.6em;">display:flex</p>

<p style="font-size:1em; text-align: left">displya:flexを指定すると子要素が横並びになる。<br>
幅を拡張するプロパティはflex:拡幅率、減幅率、基準幅</p>

* [display:flex sample](http://jsdo.it/kotaro_tan/52yO)
