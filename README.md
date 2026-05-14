# Homework 8

This homework practices CSS floats, clearfix, spacing, and CSS custom properties.

## Files

- `index.html` contains the page structure and box examples.
- `style.css` contains the layout, colors, spacing variables, float rules, and clearfix rules.

## Main CSS Ideas

The layout uses floated boxes:

```css
.box--left {
    float: left;
}

.box--right {
    float: right;
}
```

Because floated elements do not automatically give height to their parent, the parent containers use a clearfix:

```css
.section:after,
.inset-box:after {
    content: "";
    display: table;
    clear: both;
}
```

Spacing is controlled mostly with CSS variables:

```css
:root {
    --box-height: 60px;
    --box-width: 100px;
    --side-padding: 10px;
    --border-size: 2px;
}
```

The `.inset-box` width is calculated from the predefined box sizes, spacing, padding, and border size.

## Notes

- Parent `padding` creates space between a container border and its children.
- Child `margin` creates space between neighboring boxes.
- `box-sizing: border-box` makes width and height include padding and border.
- Clearfix is needed when a parent contains only floated children.
