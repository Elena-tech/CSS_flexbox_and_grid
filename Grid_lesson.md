# CSS Grid Lesson

## Introduction to CSS Grid
CSS Grid is a powerful layout system that provides a two-dimensional grid-based framework for designing web pages. Unlike Flexbox, which works in one direction (row or column), CSS Grid allows precise control over both rows and columns.

## 1. Enabling CSS Grid
To use Grid, apply `display: grid;` to a container:

```css
.container {
  display: grid;
}
```
This makes all direct children of `.container` grid items.

## 2. Defining Grid Structure
### 2.1. Columns and Rows
Use `grid-template-columns` and `grid-template-rows` to define grid structure:
```css
.container {
  display: grid;
  grid-template-columns: 200px 200px;
  grid-template-rows: 100px 100px;
}
```
This creates a 2x2 grid where columns are `200px` wide and rows are `100px` high.

### 2.2. Using `fr` Units
The `fr` unit distributes space proportionally:
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr; /* Three columns, middle one is twice as large */
}
```

## 3. Placing Grid Items
Grid items are placed using `grid-column` and `grid-row` properties:
```css
.item1 {
  grid-column: 1 / 3; /* Spans from column 1 to column 3 */
  grid-row: 1 / 2;
}
```

## 4. Common Grid Properties
| Property | Description |
|----------|------------|
| `display: grid;` | Enables Grid on a container. |
| `grid-template-columns` | Defines the number and size of columns. |
| `grid-template-rows` | Defines the number and size of rows. |
| `grid-column` | Specifies an item's position and span in columns. |
| `grid-row` | Specifies an item's position and span in rows. |
| `gap` | Adds space between grid items. |
| `justify-items` | Aligns grid items horizontally (`start`, `center`, `end`, `stretch`). |
| `align-items` | Aligns grid items vertically (`start`, `center`, `end`, `stretch`). |

## 5. Example Layouts
### 5.1. Simple Grid Layout
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 equal columns */
  gap: 10px;
}
.item {
  background-color: lightblue;
  padding: 20px;
  text-align: center;
}
```
```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>
```

### 5.2. Centering with Grid
```css
.container {
  display: grid;
  place-items: center;
  height: 300px;
  background-color: lightgray;
}
```

## 6. Grid Cheatsheet
### Spanning Multiple Columns
```css
grid-column: 1 / 3; /* Spans from column 1 to column 3 */
grid-row: 2 / 4; /* Spans from row 2 to row 4 */
```

### Aligning Items
```css
justify-items: center; /* Centers items horizontally */
align-items: center; /* Centers items vertically */
```

## 7. Conclusion
CSS Grid provides a powerful way to create responsive, flexible layouts. Understanding grid columns, rows, and placement properties will help you design modern web interfaces efficiently.
