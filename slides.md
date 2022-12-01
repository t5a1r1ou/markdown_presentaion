---
# try also 'default' to start simple
theme: unicorn
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ライトニングトーク12/1資料
# persist drawings in exports and build
drawings:
  persist: true
# use UnoCSS
css: unocss
---

# マークダウンの活用事例と書き方

〜 LightningTalk 12/1 〜

<!--
それではマークダウンの活用事例について話していきます
-->

---
class: 'text-center'
---


# マークダウンとは？

<!-- マークダウン知らない、もしくは、使ったことがないという方いらっしゃいますでしょうか？マークダウンとは -->

---
class: 'text-center'
---

# マークダウンとは文章を書くときの**記法**の一種です。

<br><br>
マークダウンを使うことで、**HTML**を簡単な記述方法で書くことができます。


<style>
p {
  font-size: 1.4rem;
}
strong {
  color: #fff !important;
}
</style>

<!--
文章を書くときの記法の一種です。マークダウンを使って書かれた文章は、エディタやビルドツール、Webサービスなどを通じてHTMLに変換がされます。
HTMLはタグがたくさんあり書き方を覚えるまでのハードルが高いですが、マークダウンはそれが簡略化されていて、覚えやすく使いやすいです。
エンジニアであってもなくても手軽にHTMLが簡単に書けるため、世の中の様々なサービスにてマークダウンは活用されています。
-->

---
class: "text-center"
---

# マークダウンの活用事例

<!-- ということで早速簡単にマークダウンの活用事例をご紹介します。　-->

---
layout: image-right
image: /images/react.png
---
活用事例①
# ドキュメント

ソフトやプログラム、ライブラリにはREADMEと呼ばれるドキュメントをつけておくことが慣習となっており、そのドキュメントは多くの場合マークダウン形式で書かれています。
<br>また、社内ではあまり見かけない気もしますが、設計書、仕様書やWikiなど、多くのドキュメントに使われるようです。

- ReactのREADME.md冒頭

```markdown
# [React](https://reactjs.org/) &middot; [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/main/LICENSE) [![npm version](https://img.shields.io/npm/v/react.svg?style=flat)](https://www.npmjs.com/package/react) [![CircleCI Status](https://circleci.com/gh/facebook/react.svg?style=shield&circle-token=:circle-token)](https://circleci.com/gh/facebook/react) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://reactjs.org/docs/how-to-contribute.html#your-first-pull-request)

React is a JavaScript library for building user interfaces.

* **Declarative:** React makes it painless to create interactive UIs. Design simple views for each state in your application, and React will efficiently update and render just the right components when your data changes. Declarative views make your code more predictable, simpler to understand, and easier to debug.
* **Component-Based:** Build encapsulated components that manage their own state, then compose them to make complex UIs. Since component logic is written in JavaScript instead of templates, you can easily pass rich data through your app and keep the state out of the DOM.
* **Learn Once, Write Anywhere:** We don't make assumptions about the rest of your technology stack, so you can develop new features in React without rewriting existing code. React can also render on the server using Node and power mobile apps using [React Native](https://reactnative.dev/).

[Learn how to use React in your project](https://reactjs.org/docs/getting-started.html).

```

<style>
  p {
    margin-top: .25rem !important;
  }
</style>

<!-- まず、ドキュメントと書いたんですけど、ソフトやプログラムのREADMEとかはよくマークダウンで書かれていますよね。社内ではそもそも設計書、仕様書というのは立場上、あまり見かけませんが、そういった多くのドキュメントで使われるようです。と調べるうちに出てきたんですけど、社内ではどうなんですかね？こちらはReactというライブラリのGitHubのページで使われている事例です。 -->


---
layout: image-left
image: /images/backlog.png
---
活用事例②
# コミュニケーション<br>ツール

よく社内で使われているBacklogやSlackですが、これらのツールでもサービス全体の様々なテキストエディタの箇所でマークダウン記法を使うことができます。

- BacklogのWiki
```markdown
# BacklogのWikiへようこそ！
Wikiを利用することで複数のユーザーでドキュメントを編集し、記録を残していくことができます。
プロジェクトの概要や必要な情報をWikiの最初のページにまとめておけば、新しいメンバーがスムーズにプロジェクトに参加できるようになるでしょう。

以下のようなドキュメントを作ってみましょう！

入門サイト、[サル先生の Wiki 入門 〜チームの情報を共有しよう〜](https://backlog.com/ja/wiki-guide/)では、Wiki についての一般的な知識と、実業務で使うための操作方法を学ぶことができます。

```

<style>
  p {
    margin-top: .5rem !important;
  }
</style>


<!-- 次に、コミュニケーションツールです。一つ目のドキュメントの事例とドキュメントという意味とあまり変わりませんが、皆さんに馴染みの深いものであるため、あえて分けてご紹介させていただきました。Backlog、Slackのテキストエディタはアイコンでテキストをリンクにしたり太字にしたりできますが、マークダウンで書いても同じことができるようになっているかと思います。 　-->

---
layout: image-right
image: /images/slidev.png
---
活用事例③
# スライド作成ツール
マークダウンを用いたスライド作成ツールは近年たくさん開発がされていて、最も有名なものに[reavel.js](https://revealjs.com/)があり、[Marp](https://marp.app/)や[MarkdownPreviewEnhanced](https://shd101wyy.github.io/markdown-preview-enhanced/#/ja-jp/)、このスライドを作るのに使っている[Slidev](https://sli.dev/)などがあります。

![](/images/slides_md.png)

<style>
  p {
    margin-top: .5rem !important;
  }
  img {
    margin-top: 2rem !important;
  }
</style>

<!-- 次に紹介するのが、スライド作成ツールです。マークダウンを用いたスライド作成ツールは結構たくさんありまして、最も有名と言われているのが、このreavel.jsや、先ほどのスライドでも出てきました、MarkdownPreviewEnhancedやちょっと似ているのが、Marpというもので、どちらもVScodeで動くツールだったりします。また、このスライドを作っているのも、こういったマークダウンを用いてスライドを作れるツールを使っていて、Slidevというツールを使っています。このSlidevは結構いろんなことができて、urlのところにpresenterと入れるとこういう発表者用のページが出てきて、台本を表示できたり、次のスライド、アニメーションが見えたり、線を引けたり。。。こちらの発表ページでも色々オプションがあって、修正ができたり、顔を出せたり、録画ができたり、また、レイアウトやアニメーションも、先ほどのMPEよりも柔軟に対応できます。ただ、slidevという名の通り、開発者のためのスライド作成ツールというコンセプトなのもあり、ちょっと作るのに開発の知識がいる場面があったりします。ので、MPEを紹介したんですが、もし、気になる方がいれば、あとでお声掛けください。エンジニアチームには公式のチュートリアルスライドを日本語訳したものとかも用意しているので、別の場でまた紹介させてください。 -->

---
layout: image-left
image: /images/astro.png
---
活用事例④
# ブログ

マークダウンの記法はブログの記事を書く際にもよく用いられます。はてなブログやWordPressでももちろん使えますし、techlabで使用しているGhostというCMSでも使えます。<br>
また最近では、AstroやGatsbyといったマークダウンファイル（.md）をビルド時にHTMLに変換し、静的HTMLを吐き出す静的サイトジェネレーターも増えてきました。
![](/images/ssg.png)


<style>
  p {
    margin-top: .25rem !important;
  }
  img {
    margin-top: 1rem !important;
  }
</style>

<!-- マークダウンの活用事例に戻ります。マークダウンはブログの記事を書くときの記法としてもよく使われます。はてなブログとか、WordPressでも使えますし、また、HMSのtechlabもGhostというCMSを使っていて、そこでもマークダウンで記事を書くことができます。
また、最近では、AstroやGatsbyのような静的サイトジェネレーターと呼ばれるツールを使って、ブログのコンテンツをドットmdという拡張子を持つ、マークダウンファイルからHTMLを生成するといったこともできます。ローカルファイルでブログ記事を管理できるので、ブログサービスのサーバー等に何らかのトラブルがあっても、安心ですよね。 　-->

---
layout: image-right
image: /images/todos.png
---
活用事例⑤
# メモ

自分用やちょっとした議事録としても、文章のフォーマットを揃えられたり、エディタの機能を使えばTODOリストが簡単にできたり、リンク付きで文章を管理できたりと意外と便利だったりします。

```markdown
# メモ

## TODO

- [ ] 掃除
- [ ] 洗濯
- [ ] 皿洗い
- [X] ~~*[ブログチェック](https://tech-lab.hakuhodo-ms.com/)*~~ [2022-12-01]
```

<style>
  p {
    margin-top: .5rem !important;
  }
  img {
    margin-top: 2rem !important;
  }
</style>

<!-- 最後に、メモとしても案外使えますということで、まあ、こんなふうにTODO管理をしたことはあんまりないんですが、ちょっとしたメモをする時なんかにも、文章のフォーマットとかもあまり考えずにスラスラと書き始めることができたりするので、意外と重宝していますし、誰かに共有する際にもマークダウンであれば、共通の認識をすることができたりします。 -->


---
class: 'text-center'
---


# でも使いこなすの難しそう...
<div v-click>
<p class="mt-5 text-xl text-orange-400">簡単です!</p>
</div>

<!-- でもあんまり使ったことがない人からすれば、「マークダウンってエンジニアがかくものなんじゃないの」とか「使いこなすの難しそうで、結局使わなさそう」といった声ももしかしたらあるかもしれないと思いましたが、[クリック]簡単です。というわけで -->

---
class: 'text-center'
---

# マークダウンの書き方

<!--　マークダウンの書き方ということで、まとめてみました。一つ注意なのが、マークダウンを書いた際にどのように表示されるかは、そのエディタ、ライブラリ、Webサービスによって生成されるHTMLに対するCSSの付け方が違うので、参考程度にしていただければと思います。　-->

---

# 見出し
h1〜h6まで書くことができます。

<div grid="~ cols-2 gap-4">
<div>

```markdown
# 見出し1

## 見出し2

### 見出し3

#### 見出し4

##### 見出し5

###### 見出し6

```
</div>
<div>

# 見出し1

## 見出し2

### 見出し3

#### 見出し4

##### 見出し5

###### 見出し6

</div>
</div>

<!--
-->

---

# 箇条書きリスト

ネストすることもできます。

<div grid="~ cols-2 gap-4">
<div>

```markdown
- item1
- item2
  - item2-1
  - item2-2

```
</div>
<div>

- item1
- item2
  - item2-1
  - item2-2

</div>
</div>

```html
<ul>
  <li>
    item1
  </li>
  <li>
    item2
    <ul>
      <li>item2-1</li>
      <li>item2-2</li>
    </ul>
  </li>
</ul>
```
このように変換されます。


<!--
-->


---

# 番号付きリスト

<div grid="~ cols-2 gap-4">
<div>

```markdown
1. meal
1. drink
  1. beer
  1. water
1. sweets

```
</div>
<div>

1. meal
2. drink
   1. beer
   2. water
3. sweets

</div>
</div>

```html
<ol>
  <li>
    meal
  </li>
  <li>
    drink
    <ol>
      <li>beer</li>
      <li>water</li>
    </ol>
  </li>
  <li>
    sweets
  </li>
</ol>
```
このように変換されます。


<!--
-->

---

# 引用

<div grid="~ cols-2 gap-4">
<div>

```markdown
>　引用です。
>
> まだ引用です。
>> 引用の中の引用です。

```
</div>
<div>

>　引用です。
>
> まだ引用です。
>> 引用の中の引用です。

</div>
</div>

```html
<blockquote>
  <p>引用です。</p>
  <p>まだ引用です。</p>
  <blockquote>
    <p>引用の中の引用です。</p>
  </blockquote>
</blockquote>
```
このように変換されます。


<!--
-->

---

# 画像

<div grid="~ cols-2 gap-4">
<div>

```markdown
![ダミー画像](https://placehold.jp/150×150.png)

```
</div>
<div>

![ダミー画像](https://placehold.jp/150×150.png)

</div>
</div>

```html
<p>
  <img src="https://placehold.jp/150%C3%97150.png" alt="ダミー画像">
</p>
```
このように変換されます。


<!--
-->

---

# 文字の装飾

<div grid="~ cols-2 gap-4">
<div>

```markdown
*斜体*です

**太字**です

***斜体かつ太字***です

~~訂正線~~です

```
</div>
<div>

*斜体*です

**太字**です

***斜体かつ太字***です

~~訂正線~~です

</div>
</div>

```html
<p>
  <em>斜体</em>です
</p>
<p>
  <strong>太字</strong>です
</p>
<p>
  <em><strong>斜体かつ太字</strong></em>です
</p>
<p>
  <s>訂正線</s>です
</p>
```
このように変換されます。


<!--
-->
---

# テーブル

<div grid="~ cols-2 gap-4">
<div>

```markdown
name | age
-|-
bob | 15
```
</div>
<div>

name | age
-|-
bob | 15

</div>
</div>

```html
<table>
  <thead>
    <tr>
      <th>name</th>
      <th>age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>bob</td>
      <td>15</td>
    </tr>
  </tbody>
</table>
```
このように変換されます。


<!--
-->


---
class: 'text-center -translate-y-10'
---

# こちらのYoutube動画もおすすめです

<div>
  <Youtube id="tjygVZLLeYc" class="mx-auto scale-150 translate-y-10" />
</div>

<!-- これらの書き方をまとめたところに関しては、こちらのyoutubeの動画を参考にしていますので、もし、もっとちゃんと知りたいという方は、こちらの動画もおすすめです。 -->


---
layout: center
class: text-center
---

# ありがとうございました。

<!-- ご清聴いただきありがとうございました！ -->
