# CSS Grid notes:

- Requires a wrapper div

```html
<div class="grid">
  some text
</div>
```
- ``display: grid`` on wrapper class defines it as a grid
- ``grid-template-columns`` defines number and size of columns
- ``grid-column-gap`` defines space between columns
- ``grid-row-gap`` defines space between rows
- ``grid-gap`` defines space between columns and rows

```css
.grid {
  display: grid;
  grid-template-columns: 70% 30%;
  grid-gap: 1em;
}
```

- The recommended way to define columns is to use fractions instead of percentages, since percentages will cause issues with margin and padding

```css
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```

- There's some shorthand for this that can make it much easier to edit your columns

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```

- This will create 3 columns of 1fr
- You can also use repeat to create multiple columns of differing sizes

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr 2fr);
}
```

- ``grid-auto-rows`` is used to define the size of each row
- This gives a height of 100px to each row

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr 2fr);
  grid-auto-rows: 100px;
}
```

- However, this isn't flexible and won't adjust to content
- The following example is a better way to have flexible height.
- Here, the minimum row height is set to 100px, but will increase the height if the content demands it

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr 2fr);
  grid-auto-rows: minmax(100px, auto);
}
```
