---
title: '-ms-scrollbar-base-color'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollbarColor.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollbarBaseColor.htm'
notes:
  - 'Add summery, values, specifications, compatibility.'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/properties
    href: /css/properties
standardization_status: Non-Standard
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: css/properties/-ms-scrollbar-base-color

---
Property of [css/properties](/css/properties)[css/properties](/css/properties)

## Syntax

``` js
var result = element.-ms-scrollbar-base-color;
element.-ms-scrollbar-base-color = value;
```

## Examples

The following example shows how to create a style rule that sets the **-ms-scrollbar-base-color** property for a **textArea** element.

``` html
<HTML>
  <HEAD>
    <STYLE>
        TEXTAREA.BlueScrollbar  { scrollbar-base-color:blue }
    </STYLE>
  </HEAD>
  <BODY>
    <TEXTAREA CLASS="BlueScrollbar">The scroll bar for
    this element will be blue.</TEXTAREA>
  </BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollbarColor.htm)

The following style rule uses the **-ms-scrollbar-base-color** attribute as part of a coordinated color theme. Earth tones are specified for all the elements defined in the style rule.

``` html
<STYLE>
  BODY { scrollbar-base-color:darkolivegreen; background-color:tan }
  H1 { color:bisque }
  P { color:darkslategray }
</STYLE>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollbarBaseColor.htm)

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-scrollbar-base-color** attribute is an extension to CSS, and can be used as a synonym for **scrollbar-base-color** in IE8 Standards mode. The scroll box is the square box within a scroll bar that can be moved either up and down or left and right on a track to change the position of the content on the screen. The scroll arrows, located at each end of a scroll bar, are the square buttons containing the arrows that move the content on the screen in small increments, either up and down or left and right. This property applies to elements that display a scroll bar. Cascading Style Sheets (CSS) enable scrolling on all objects through the [**overflow**](/css/properties/overflow) property. These objects are not listed in the Applies To list for this property. The **-ms-scrollbar-base-color** property is a composite property. You can use separate properties to specify each of the individual properties, but in many cases it is more convenient to set them in one place using this composite property.

### Syntax

`-ms-scrollbar-base-color: variant`

### Standards information

There are no standards that apply here.

## See also

### Related articles

#### Scrollbar

-   [-ms-scrollbar-3d-light-color](/css/properties/-ms-scrollbar-3d-light-color)

-   [-ms-scrollbar-arrow-color](/css/properties/-ms-scrollbar-arrow-color)

-   **-ms-scrollbar-base-color**

-   [-ms-scrollbar-darkshadow-color](/css/properties/-ms-scrollbar-darkshadow-color)

-   [-ms-scrollbar-face-color](/css/properties/-ms-scrollbar-face-color)

-   [-ms-scrollbar-highlight-color](/css/properties/-ms-scrollbar-highlight-color)

-   [-ms-scrollbar-shadow-color](/css/properties/-ms-scrollbar-shadow-color)

-   [-ms-scrollbar-track-color](/css/properties/-ms-scrollbar-track-color)

### Related pages

-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaultSelected[defaultSelected](/dom/HTMLOptionElement/defaultSelected)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   `Reference`
-   -ms-scrollbar-3dlight-color[-ms-scrollbar-3dlight-color](/css/properties/-ms-scrollbar-3d-light-color)
-   -ms-scrollbar-arrow-color[-ms-scrollbar-arrow-color](/css/properties/-ms-scrollbar-arrow-color)
-   -ms-scrollbar-darkshadow-color[-ms-scrollbar-darkshadow-color](/css/properties/-ms-scrollbar-darkshadow-color)
-   -ms-scrollbar-face-color[-ms-scrollbar-face-color](/css/properties/-ms-scrollbar-face-color)
-   -ms-scrollbar-highlight-color[-ms-scrollbar-highlight-color](/css/properties/-ms-scrollbar-highlight-color)
-   -ms-scrollbar-shadow-color[-ms-scrollbar-shadow-color](/css/properties/-ms-scrollbar-shadow-color)
-   -ms-scrollbar-track-color[-ms-scrollbar-track-color](/css/properties/-ms-scrollbar-track-color)
