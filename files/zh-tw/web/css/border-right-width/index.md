---
title: border-right-width
slug: Web/CSS/border-right-width
tags:
  - CSS
  - CSS Borders
  - CSS Property
  - Reference
  - recipe:css-property
browser-compat: css.properties.border-right-width
translation_of: Web/CSS/border-right-width
---
{{CSSRef}}

**`border-right-width`** 是一種CSS屬性，用來設定元件右側[邊框](/zh-TW/docs/Web/CSS/border)的粗細。

{{EmbedInteractiveExample("pages/css/border-right-width.html")}}

## 語法

```css
/* Keyword values */
border-right-width: thin;
border-right-width: medium;
border-right-width: thick;

/* <length> values */
border-right-width: 10em;
border-right-width: 3vmax;
border-right-width: 6px;

/* Global keywords */
border-right-width: inherit;
border-right-width: initial;
border-right-width: revert;
border-right-width: revert-layer;
border-right-width: unset;
```

### 屬性值

- `<line-width>`

  - : 定義邊框寬度。屬性值需宣告為{{cssxref("&lt;length&gt;")}}的非負數數值，或以下特定字串：

    - `thin`
    - `medium`
    - `thick`

> **注意:** 因為規範文件沒有明確定義每個特定字串所代表的精確數值，所以使用特定字串宣告所得到的任何邊框寬度都算符合文件規範。儘管特定字串對應邊框寬度的規範並不明確，但三者關係通常遵循規則`thin ≤ medium ≤ thick`，且在同個文件中相同字串會對應相同的邊寬數值。

## Formal definition 標準定義

{{CSSInfo}}

## Formal syntax 語法規則

{{csssyntax}}

## 範例

### 邊框粗細對比

#### HTML

```html
<div>元件 1</div>
<div>元件 2</div>
```

#### CSS

```css
div {
  border: 1px solid red;
  margin: 1em 0;
}

div:nth-child(1) {
  border-right-width: thick;
}
div:nth-child(2) {
  border-right-width: 2em;
}
```

#### 成果

{{EmbedLiveSample('邊框粗細對比', '100%')}}

## 規範

{{Specifications}}

## 瀏覽器相容性

{{Compat}}

## 參見

- 與框線粗細相關的其他屬性：{{Cssxref("border-bottom-width")}}、{{Cssxref("border-left-width")}}、{{Cssxref("border-top-width")}}和{{Cssxref("border-width")}}。
- 與右側框線相關的其他簡寫屬性：{{Cssxref("border")}}、{{Cssxref("border-right")}}、{{Cssxref("border-right-style")}}和{{Cssxref("border-right-color")}}。
