# Coding Rule


## Environment

**tab** : space 2 length



## HTML

✎**Document**  
Language Japanese
``<html lang="ja">``

✎**External link**  
外部サイトへのリンクには``rel="noreffere noopener"``を付与してください。  
``<a href="" target="_blank">...</a>``  
External link with ``rel="noreffere noopener"`` add params


✎**Image file format**  
画像ファイルフォーマット  
ピクセル画像は``type/png`` ``type/jpeg``  
ベクター画像は``svg(XML)``  
photo, pixel image is use ``type/png`` ``type/jpeg``  export scale 1.5x
vector image is use ``svg(XML)``


✎**use svg**  
svgを利用する場合は以下の2つの方法を使ってください。  
not write in HTML Document
use ``<img src="">`` or ``<use href="">`` in path

✎**input wrapper use label and fieldset**  
```html
<fieldset>
  <input type="checkbox" id="CHECKBOX_NAME" name="" value="" />
  <label id="CHECKBOX_NAME">On Click</label>
</fieldset>
or
<fieldset>
  <label id="CHECKBOX_NAME">
	<input type="checkbox" id="CHECKBOX_NAME" name="" value="" />
    <span>On Click</span>
  </label>
</fieldset>
```



## StyleSheet

✎**Post CSS** : Sass | Scss  
✎**Rule** : BEM | SMACSS | FLOCSS

✎**Separate by parts**  
コンポーネント単位でsassファイルを作成してください。  

```css
// header.scss
.header {
  background-color: #ccc;
  &--wrap {
    padding: 20px;
  }
}

// footer.scss
.footer {
  background-color: #ccc;
  &--wrap {
    padding: 20px;
  }
}
```

✎**Not use !important**  

!importantは使わずに、ネストで有効にしてください。  
not foce extends style  


✎**No HTML specified**  
直接HTMLを指定せず。クラス名で指定してください。  
write except for reset style 
```html
<!-- HTML -->
<p class="text">...</p>

<!-- Stylesheet -->
p { font-size: 18px; } <!-- no specify TagName -->
↓↓↓
.text { font-size: 18px; } <!-- specify class name -->
```

✎**Mouse action trigger DOM cursor type**  
``div`` ``p`` ``span`` etc...   add ``cursor: pointer``

✎**Use Grid Layout**  
``display: grid``

✎**Media query**  
メディアクエリは指定したスタイルの記述の中で記述してください。  
nest in write media query params
```css
.header {
  padding: 28px;
 
  @media screen and max-width(768px) {
    padding: 18px;
  }

  &--inner {
    max-width: 1080px;
 
    @media screen and max-width(768px) {
      max-width: 96vw;
    }
  }
}
```



### Responsive
フレキシブルにコーディングを行ってください。  
デザインファイルにあるアートボードサイズの時は、  
デザイン通りにコーディングしてください。  
Flexible Layout





## Javascript

✎**webpack** : Babel, ES6



## Other
