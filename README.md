# CSS Grid notes:

- Requires a wrapper div

```html
<div class="grid">
  some text
</div>
```
- display:grid on wrapper class defines it as a grid
- grid-template-columns defines number and size of columns
- grid-column-gap defines space between columns
- grid-row-gap defines space between rows
- grid-gap defines space between columns and rows

```css
.grid {
  display: grid;
  grid-template-columns: 70% 30%;
  grid-gap: 1em;
}
```
