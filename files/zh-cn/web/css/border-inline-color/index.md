---
title: border-inline-color
slug: Web/CSS/border-inline-color
---

{{CSSRef}}

The **`border-inline-color`** [CSS](/zh-CN/docs/Web/CSS) property defines the color of the logical inline borders of an element, which maps to a physical border color depending on the element's writing mode, directionality, and text orientation. It corresponds to the {{cssxref("border-top-color")}} and {{cssxref("border-bottom-color")}}, or {{cssxref("border-right-color")}} and {{cssxref("border-left-color")}} property depending on the values defined for {{cssxref("writing-mode")}}, {{cssxref("direction")}}, and {{cssxref("text-orientation")}}.

```css
border-inline-color: yellow;
border-inline-color: #F5F6F7;
```

The border color in the other dimension can be set with {{cssxref("border-block-color")}} which sets {{cssxref("border-block-start-color")}}, and {{cssxref("border-block-end-color")}}.

## Syntax

### Values

- `<'color'>`
  - : The color of the border. See {{cssxref("color")}}.

## Formal definition

{{CSSInfo}}

## Formal syntax

{{csssyntax}}

## Examples

### Border color with vertical text

#### HTML

```html
<div>
  <p class="exampleText">Example text</p>
</div>
```

#### CSS

```css
div {
  background-color: yellow;
  width: 120px;
  height: 120px;
}

.exampleText {
  writing-mode: vertical-lr;
  border: 10px solid blue;
  border-inline-color: red;
}
```

#### Results

{{EmbedLiveSample("Border_color_with_vertical_text", 140, 140)}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat("css.properties.border-inline-color")}}

## See also

- This property maps to the physical border properties: {{cssxref("border-top-color")}}, {{cssxref("border-right-color")}}, {{cssxref("border-bottom-color")}}, or {{cssxref("border-left-color")}}.
- {{cssxref("writing-mode")}}, {{cssxref("direction")}}, {{cssxref("text-orientation")}}+ bug 1297097
