# Flexbox Lesson

## Introduction to Flexbox
Flexbox (Flexible Box Layout) is a CSS layout model that allows items to align and distribute space efficiently inside a container. It provides an easy way to create responsive layouts without relying on floats or positioning.

## 1. Enabling Flexbox
To use Flexbox, apply `display: flex;` to a container:

```css
.container {
  display: flex;
}
```

This makes all direct children of `.container` flex items.

## 2. Main Axis & Cross Axis
- **Main Axis**: Defined by `flex-direction`, it can be `row` (default) or `column`.
- **Cross Axis**: Perpendicular to the main axis.

## 3. Flexbox Properties
### 3.1. Container Properties

| Property | Description |
|----------|------------|
| `display: flex;` | Enables Flexbox on a container. |
| `flex-direction` | Defines the main axis direction (`row`, `row-reverse`, `column`, `column-reverse`). |
| `justify-content` | Aligns items along the main axis (`flex-start`, `center`, `flex-end`, `space-between`, `space-around`, `space-evenly`). |
| `align-items` | Aligns items along the cross axis (`flex-start`, `center`, `flex-end`, `stretch`, `baseline`). |
| `align-content` | Aligns multiple flex lines (`flex-start`, `center`, `flex-end`, `space-between`, `space-around`, `stretch`). |
| `flex-wrap` | Controls item wrapping (`nowrap`, `wrap`, `wrap-reverse`). |

### 3.2. Flex Item Properties

| Property | Description |
|----------|------------|
| `flex-grow` | Defines how an item grows relative to others. |
| `flex-shrink` | Defines how an item shrinks relative to others. |
| `flex-basis` | Sets the initial size of an item before growing/shrinking. |
| `align-self` | Overrides `align-items` for individual items (`auto`, `flex-start`, `center`, `flex-end`, `stretch`). |
| `order` | Specifies item order within the container. |

## 4. Example Layouts
### 4.1. Basic Flexbox Layout
```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.item {
  width: 100px;
  height: 100px;
  background-color: lightblue;
}
```
```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>
```

### 4.2. Centering Items
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 300px;
  background-color: lightgray;
}
```

## 5. Flexbox Cheatsheet
### Justify Content
```css
justify-content: flex-start;  /* Aligns items to start */
justify-content: flex-end;    /* Aligns items to end */
justify-content: center;      /* Aligns items to center */
justify-content: space-between; /* Spaces items evenly */
justify-content: space-around; /* Adds equal space around items */
justify-content: space-evenly; /* Spaces items with equal gaps */
```

### Align Items
```css
align-items: flex-start;  /* Aligns items to start of cross axis */
align-items: flex-end;    /* Aligns items to end of cross axis */
align-items: center;      /* Centers items along cross axis */
align-items: stretch;     /* Stretches items to fill container */
```

## 6. Conclusion
Flexbox is a powerful layout system that simplifies responsive design. Mastering `flex-direction`, `justify-content`, and `align-items` will allow you to build dynamic and adaptable layouts.

