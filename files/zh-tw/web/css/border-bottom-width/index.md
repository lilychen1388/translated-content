---
title: border-bottom-width
slug: Web/CSS/border-bottom-width
tags:
  - CSS
  - CSS Borders
  - CSS Property
  - Reference
  - recipe:css-property
browser-compat: css.properties.border-bottom-width
translation_of: Web/CSS/border-bottom-width
---
{{CSSRef}}

**`border-bottom-width`** 是一種CSS屬性，用來設定元件下側[邊框](/zh-TW/docs/Web/CSS/border)的粗細。

{{EmbedInteractiveExample("pages/css/border-bottom-width.html")}}

## 語法

```css
/* Keyword values */
border-bottom-width: thin;
border-bottom-width: medium;
border-bottom-width: thick;

/* <length> values */
border-bottom-width: 10em;
border-bottom-width: 3vmax;
border-bottom-width: 6px;

/* Global keywords */
border-bottom-width: inherit;
border-bottom-width: initial;
border-bottom-width: revert;
border-bottom-width: revert-layer;
border-bottom-width: unset;
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

### 下側邊框粗細對比

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
  border-bottom-width: thick;
}
div:nth-child(2) {
  border-bottom-width: 2em;
}
```

#### 成果

{{EmbedLiveSample('下側邊框粗細對比', '100%')}}

## 規範

{{Specifications}}

## 瀏覽器相容性

{{Compat}}

## 參見

- 與框線粗細相關的其他屬性：{{Cssxref("border-left-width")}}、{{Cssxref("border-right-width")}}、{{Cssxref("border-top-width")}}和{{Cssxref("border-width")}}。
- 與下側框線相關的其他簡寫屬性：{{Cssxref("border")}}、{{Cssxref("border-bottom")}}、{{Cssxref("border-bottom-style")}}和{{Cssxref("border-bottom-color")}}。
