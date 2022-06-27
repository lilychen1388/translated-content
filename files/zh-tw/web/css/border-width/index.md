---
title: border-width
slug: Web/CSS/border-width
tags:
  - CSS
  - CSS Borders
  - CSS Property
  - Reference
  - recipe:css-shorthand-property
browser-compat: css.properties.border-width
translation_of: Web/CSS/border-width
---
{{CSSRef}}

**`border-width`** 是一種[CSS](/zh-TW/docs/Web/CSS)[簡寫屬性](/zh-TW/docs/Web/CSS/Shorthand_properties)，用來綜合設定元件四邊框線的粗細大小。

{{EmbedInteractiveExample("pages/css/border-width.html")}}

## Constituent properties 屬性組成

border-width簡寫的屬性值內容由以下CSS的屬性值構成。

- [`border-bottom-width`](/zh-TW/docs/Web/CSS/border-bottom-width)
- [`border-left-width`](/zh-TW/docs/Web/CSS/border-left-width)
- [`border-right-width`](/zh-TW/docs/Web/CSS/border-right-width)
- [`border-top-width`](/zh-TW/docs/Web/CSS/border-top-width)

## 語法

```css
/* Keyword values */
border-width: thin;
border-width: medium;
border-width: thick;

/* <length> values */
border-width: 4px;
border-width: 1.2rem;

/* vertical | horizontal */
border-width: 2px 1.5em;

/* top | horizontal | bottom */
border-width: 1px 2em 1.5cm;

/* top | right | bottom | left */
border-width: 1px 2em 0 4rem;

/* Global values */
border-width: inherit;
border-width: initial;
border-width: revert;
border-width: revert-layer;
border-width: unset;
```

`border-width` 屬性值可設定一到四個輸入值。

- 一個值：將單一數值指定給**全部四個邊**作為邊寬。
- 兩個值：依數值排列順序，分別指定邊寬給：**上下邊**、**左右邊**。
- 三個值：依數值排列順序，分別指定邊寬給：**上邊框**、**左右邊**、**下邊框**。
- 四個值：依數值排列順序，沿邊框順時鐘方向，分別指定給：**上邊框**、**右邊框**、**下邊框**、**左邊框**。

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

### 長度數值混合宣告示範

#### HTML

```html
<p id="sval">
    一個輸入值：四個邊寬全設為 6px</p>
<p id="bival">
    兩個輸入值且值互不相等：上下邊寬2px；左右邊寬10px</p>
<p id="treval">
    三個輸入值且值互不相等：上邊寬0.3em；左右邊寬為零；下邊寬9px</p>
<p id="fourval">
    四個輸入值且值互不相等：上邊寬設為"thin"；右邊寬為"medium"；下邊寬為"thick"；左邊寬1em</p>
```

#### CSS

```css
#sval {
  border: ridge #ccc;
  border-width: 6px;
}
#bival {
  border: solid red;
  border-width: 2px 10px;
}
#treval {
  border: dotted orange;
  border-width: 0.3em 0 9px;
}
#fourval {
  border: solid lightgreen;
  border-width: thin medium thick 1em;
}
p {
  width: auto;
  margin: 0.25em;
  padding: 0.25em;
}
```

#### 成果

{{ EmbedLiveSample('長度數值混合宣告示範', 320, 320) }}

## 規範

{{Specifications}}

## 瀏覽器相容性

{{Compat}}

## 參見

- 與框線相關的簡寫屬性：{{Cssxref("border")}}、{{Cssxref("border-style")}}、{{Cssxref("border-color")}}
- 與框線粗細相關的其他屬性：{{Cssxref("border-bottom-width")}}、{{Cssxref("border-left-width")}}、{{Cssxref("border-right-width")}}、{{Cssxref("border-top-width")}}
