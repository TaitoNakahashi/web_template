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
	* BEMを使用します。

## 改行コード
`LF`

## 文字コード
`UTF-8`

## インデント
`半角スペース2つ`


* ### HTMLについて
	* HTML5で記述する
	* <head></head>内の構成は専用のテンプレートを基準とする
	* 文書構造として正しいマークアップを心がける
	* 不必要なタグは削除する

* ### CSSについて
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

* ### 画像の命名ルール
	* BEMに基づく（classと同じ考え方）
	* [モジュール名]\__[要素名(複数可)]--[修飾子(複数可)]--[連番]--[状態].[拡張子]
		> 例）setting-list__item--active--01--on.png
		<br> モジュール名：モジュールのclass名を使用（setting-listなど）
		<br> 要素名：モジュールの要素名を使用（itemなど）
		<br> 修飾子：モジュールの修飾子を使用（activeなど）※ない場合は省略可
		<br> 連番：複数必要な場合は連番で管理する（01～99）※ない場合は省略可
		<br> 状態：画像の状態を示す（onなど）※ない場合は省略可

## ディレクトリ基本構成
 PDFファイルを参照してください。
<br>
[ディレクトリ基本構成](/Users/icoma/www/web_template/ディレクトリ構成.pdf)
