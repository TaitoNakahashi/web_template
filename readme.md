# SJCコーディングルール ver.1.0
#### 2018年4月18日更新

---

## 対象ブラウザ
*  **Microsoft Windows10**
	* Google Chrome
	* Mozilla Firefox
	* Microsoft Edge
	* (Internet Explorer 11) ※必要な場合のみ
* **macOS**
	* Google Chrome
	* Mozilla Firefox
	* Safari
* **Android**
	* Android Google Chrome
	* Android Browser
* **iOS**
	* Safari

## 改行コード
`LF`

## 文字コード
`UTF-8`

## インデント
`半角スペース2つ`


## HTMLについて
* HTML5で記述する
* 全て小文字で書く
* <head></head>内の構成は専用のテンプレートを基準とする
* 文書構造として正しいマークアップを心がける
* 不必要なタグは削除する

## CSSについて
* Sassで記述する
* スタイルは全てclassで指定する（id又は要素やstyle属性による直接指定は禁止）
	> js用のid指定はOK
	<br> js用のid名には必ず先頭に「js-」を付ける

* classのBEM命名はBEMに基づく
	> [モジュール名]\__[要素名(複数可)]--[修飾子(複数可)]
	<br> 例）setting-list__item--active

* 命名にキャメルケースは禁止（画像の命名ルールと合わせるため）
	> NG）settingList　←キャメルケース
	<br> OK）setting-list　←必ず「\_」ではなく「-」でつなぐこと

* マルチクラスは原則禁止（個別CSSのみOK）
* スタイルの上書き（打消し）は原則禁止（個別CSSのみOK）
* !importantは原則禁止（個別CSSのみOK）
* 入れ子の指定は原則禁止（個別CSSのみOK）
	> モジュールの中にモジュールが組み込まれ、モジュールの一部として機能する場合は、入れ子によるスタイルの上書き（打消し）をOKとする。

* body直下（.wrapper直下）のタグに割り当てるclass名は下記に統一する
	```
	.header(<header class=”header”></header>)
	.wrapper（<div class=”wrapper”></div>）※divでなくてもOK
	.content（<div class=”content”></div>）※divでなくてもOK
	.side（<div class=”side”></div>）※divでなくてもOK
	.footer（<footer class=”footer”></footer>）
	```

## Sassについて
* SCSS法で記述する
* 全て小文字で書く
* @extendはmodifierのみ使用OK
* 「common.scss」に全てのscssファイルをまとめ「common.css」のみを書き出す
書き出されないscssファイルにはファイル名の先頭に「_」を付ける
* scssファイルは「/assets/_scss」フォルダに入れる
* cssファイルは「/assets/css」フォルダに入れる（書き出す）
* 書き出しスタイルは「compressed」（空白など全て取り圧縮したスタイル）にする
* 書き出しにコメントを含めない
* 書き出しにソースマップファイルを含めない


## 画像の命名ルール
* BEMに基づく（classと同じ考え方）
* [モジュール名]\__[要素名(複数可)]--[修飾子(複数可)]--[連番]--[状態].[拡張子]
	> 例）setting-list__item--active--01--on.png
	<br> モジュール名：モジュールのclass名を使用（setting-listなど）
	<br> 要素名：モジュールの要素名を使用（itemなど）
	<br> 修飾子：モジュールの修飾子を使用（activeなど）※ない場合は省略可
	<br> 連番：複数必要な場合は連番で管理する（01～99）※ない場合は省略可
	<br> 状態：画像の状態を示す（onなど）※ない場合は省略可

## ディレクトリ基本構成
<img width="450" alt="ディレクトリ構成表" src="/readme-image.png">
