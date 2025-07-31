# How to create tables?
Obsidian works with both markdown-style and HTML-style tables. 
- markdown tables are easier to adjust but less customizable
- if you need full control, HTML tables are the way to go

## example markdown-table --> easy but with limited customization


```markdown
| key      | action               |
| -------- | -------------------- |
| Ctrl + , | open settings        |
| Ctrl + P | open command palette |
```
### output table

| key      | action               |
| -------- | -------------------- |
| Ctrl + , | open settings        |
| Ctrl + P | open command palette |



## example HTML-table --> complex but with flexible column width

```html
<table style="width:70%">
  <colgroup>
    <col style="width:40%">
    <col style="width:60%">
  </colgroup>
  <thead>
    <tr>
      <th>key</th>
      <th>action</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ctrl + ,</td>
      <td>open settings</td>
    </tr>
    <tr>
      <td>Ctrl + P</td>
      <td>open command palette</td>
    </tr>
  </tbody>
</table>
```

### output table

<table style="width:70%">
  <colgroup>
    <col style="width:40%">
    <col style="width:60%">
  </colgroup>
  <thead>
    <tr>
      <th>key</th>
      <th>action</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ctrl + ,</td>
      <td>open settings</td>
    </tr>
    <tr>
      <td>Ctrl + P</td>
      <td>open command palette</td>
    </tr>
  </tbody>
</table>