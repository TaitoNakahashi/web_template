# フロントエンドコーディング規約

## クラス名の付け方
BEMを使用します。

### Block
親の要素となるような要素をBlockとして命名します。

```css:Block
.item
.item-list
.form
.form-search
.form-search-item /* ブロック名は２つ以上単語が繋がる場合があります */
```

### Element
Element は Block に内包される部品です。Element が集まったものがBlockになるので、Element は Block 内部に存在します。
```css:Element
.item__text
.item-list__btn
.form__input
.form-search__title
.form-search-item__user
```

### Modifier（モディファイア）
Modifier は状態を表すときに使用されます。同じ部品、同じ Block や Element で色だけ変えたい場合など Modifier を使用します。
```css:Modifier
.item--red
.item-list__btn--type_success /* btnエレメントのうち、typeのキーがsuccessのモノ */
.form__input--active
.form-search__title--hover
.form-search-result__user--following
```

## 単語のセパレータ

### 単語の区切り
単語の区切りには - を利用します。
```css
.main-content /*単語からなるクラスをハイフンを使って表現します。*/
```
