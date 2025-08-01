---
title: CSS images
slug: Web/CSS/CSS_images
page-type: css-module
spec-urls:
  - https://drafts.csswg.org/css-images/
  - https://drafts.csswg.org/css-images-4/
sidebar: cssref
---

The **CSS images** module defines the types of images that can be used (the {{CSSxRef("&lt;image&gt;")}} type, containing URLs, gradients and other types of images), how to resize them and how they, and other replaced content, interact with the different layout models.

## Reference

### Properties

- {{CSSxRef("image-orientation")}}
- {{CSSxRef("image-rendering")}}
- {{CSSxRef("image-resolution")}}
- {{CSSxRef("object-fit")}}
- {{CSSxRef("object-position")}}

### Functions

- {{CSSxRef("gradient/linear-gradient", "linear-gradient()")}}
- {{CSSxRef("gradient/radial-gradient", "radial-gradient()")}}
- {{CSSxRef("gradient/repeating-linear-gradient", "repeating-linear-gradient()")}}
- {{CSSxRef("gradient/repeating-radial-gradient", "repeating-radial-gradient()")}}
- {{CSSxRef("gradient/conic-gradient", "conic-gradient()")}}
- {{CSSxRef("gradient/repeating-conic-gradient", "repeating-conic-gradient()")}}
- {{CSSxRef("cross-fade", "cross-fade()")}}
- {{CSSxRef("element", "element()")}}
- {{CSSxRef("image/image-set", "image-set()")}}

The specification also defines the {{CSSxRef("image/image", "image()")}} function, which is not yet supported by any browser.

### Data types

- {{CSSxRef("&lt;gradient&gt;")}}
- {{CSSxRef("&lt;image&gt;")}}

## Guides

- [Using CSS gradients](/en-US/docs/Web/CSS/CSS_images/Using_CSS_gradients)
  - : Presents a specific type of CSS images, _gradients_, and how to create and use these.

- [Implementing image sprites in CSS](/en-US/docs/Web/CSS/CSS_images/Implementing_image_sprites_in_CSS)
  - : Describes the common technique grouping several images in one single document to save download requests and speed up the availability of a page.

- [Styling replaced elements](/en-US/docs/Web/CSS/CSS_images/Replaced_element_properties)
  - : Introduces the properties that only apply to _replaced elements_.

- [Understanding aspect ratios](/en-US/docs/Web/CSS/CSS_box_sizing/Understanding_aspect-ratio)
  - : Learn about the `aspect-ratio` property, discuss aspect ratios for replaced and non-replaced elements, and examine some common aspect ratio use cases.

## Related concepts

- {{cssxref("url_value", "&lt;url&gt;")}}
- {{cssxref("url_function", "url()")}}

## Specifications

{{Specifications}}

## See also

- [CSS filter effects](/en-US/docs/Web/CSS/CSS_filter_effects) module
- [CSS compositing and blending](/en-US/docs/Web/CSS/CSS_compositing_and_blending) module
- [CSS colors](/en-US/docs/Web/CSS/CSS_colors) module
- [CSS values and units](/en-US/docs/Web/CSS/CSS_Values_and_Units) module
