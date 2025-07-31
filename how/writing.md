# How to write Obsidian?
This table lists key elements in the markdown-based syntax used in Obsidian. 

| goal                                                        | syntax                                                                                                                                                                            |
| ----------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| create header of target level                               | \- starting a new line with one or several `#`-symbol(s) and adding a ` `space creates a section header<br>\- the more `#`-symbols, the lower its hierarchy level                 |
| create bullet list                                          | start new line with `- ` and hit `Enter` at line end to create new item                                                                                                           |
| create numbered list                                        | start new line with `1. ` and hit `Enter` at line end to create new item                                                                                                          |
| create code block                                           | enclose code with 3 apostrophes (\` ) at code start & end<br>write coding language next to starting apostrophes<br>```python<br>print("The title of this note is", @title)<br>``` |
| convert text to boldface                                    | select target text and type ** to enclose that text with double-stars                                                                                                             |
| create link to any content, can also be outside of Obsidian | [display_name](link_url)                                                                                                                                                          |
| create link to other note in Obsidian                       | [[name_of_other_note]]                                                                                                                                                            |
| create link to section inside other note in Obsidian        | [[name_of_other_note#name_of_section\|display_name_of_section]]                                                                                                                   |
| embed content of one note into another note in Obsidian     | ![embedded_filename#optional_section]                                                                                                                                             |

## How to embed images?
Images can be pasted from the clipboard (Ctrl+C / Ctrl+V) and also accessed by their relative path starting from vault root. 

Ctrl+V will
1. create an embedding link `![[Pasted image 20250516084207.png]]` and
2. store that pasted image in the attachments folder (see setup section on [Files and Links, Define attachment folder](setup.md#files-and-links-define-attachment-folder))

### Use `|width_in_pixels` to set image width
- To adjust the display size of an image, you can add `|width_in_pixels` after the filename: 
- `![[Pasted image 20250516084207.png|300]]`

<div>
  <img src="../pics/image-width-in-pixels.png" width="500">
</div>

### Limitation and Workaround

- Limitation: Images accessed from external URL cannot be rescaled directly into obsidian
- Workaround: Since rescaling requires a locally stored image, download or take a screenshot. 

### use HTML syntax to place multiple images side-by-side

```html
<div>
  <img src="../pics/graph-view-filter-path.png" width="200">
  <img src="../pics/graph-view-pt.png" width="200">
</div>
```

<div>
  <img src="../pics/graph-view-filter-path.png" width="200">
  <img src="../pics/graph-view-pt.png" width="200">
</div>

## How to create tables?
Obsidian works with both markdown-style and HTML-style tables. 
- markdown tables are easier to adjust but less customizable
- if you need full control, HTML tables are the way to go

### example markdown-table --> easy but customization limited 


```markdown
| key      | action               |
| -------- | -------------------- |
| Ctrl + , | open settings        |
| Ctrl + P | open command palette |
```
#### output table

| key      | action               |
| -------- | -------------------- |
| Ctrl + , | open settings        |
| Ctrl + P | open command palette |



### example HTML-table --> complex but flexible column width

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

#### output table

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


## How to rearrange your content? 
Once your second brain starts growing, refactoring becomes a topic. 
There are several ways to keep your vault clean. 

### Rearrange files within your vault

Move file/folder to...

<div>
  <img src="../pics/move-file-to.png" width="300">
</div>

### Rearrange sections within a file

Drag and drop sections in right panel (aka in the outline).

<table style="border-collapse: collapse;">
  <tr>
    <td style="border: 1px solid black; text-align: center;">
      <div style="font-weight: bold; margin-bottom: 0.5em;">Step 1</div>
      <img src="../pics/writing-drag-and-drop-1.png" width="300">
    </td>
    <td style="border: 1px solid black; text-align: center;">
      <div style="font-weight: bold; margin-bottom: 0.5em;">Step 2</div>
      <img src="../pics/writing-drag-and-drop-2.png" width="300">
    </td>
    <td style="border: 1px solid black; text-align: center;">
      <div style="font-weight: bold; margin-bottom: 0.5em;">Step 3</div>
      <img src="../pics/writing-drag-and-drop-3.png" width="300">
    </td>
  </tr>
</table>


## How to use templates?

### How to build a template to manually add into a note?

If you use recurring design patterns like for example code blocks, using templates can make your life easier. 

Here's how you can setup a template to create the below python code block.

1. create template file inside template folder

<div>
  <img src="../pics/template-code-python.png" width="400">
</div>

2. link that template to a custom hotkey

<div>
  <img src="../pics/template-code-python-hotkey.png" width="500">
</div>

2. paste template content into current note by using hotkey (Ctrl + Shift + P)
```python
# this empty code block template was created by using a hotkey
```

### How to build a daily note template?

This section contains sample blocks from my daily note template which could inspire yours as well. 
#### links

While creating a note from a template with Templater code, that code will be converted into its output (=parsed) in that very moment. 

Today for example, the line
- Previous day: `[[<% tp.date.now("yyyy-MM-DD ddd", -1) %>]]`

was converted into a link to yesterdays daily note
- Previous day: [[2025-07-26 Sat]]

##### greyed out links

Since tomorrows daily note does not exist yet, the line below gets converted into a greyed out link 
- Next day: `[[<% tp.date.now("yyyy-MM-DD ddd", 1) %>]]`
- Next day: [[2025-07-28 Mon]]

<div><img src="../pics/daily-note-links-existing-and-greyed-out.png" width="300"></div>

**CAREFUL!!** 
- If you click onto a greyed-out link, you create an empty file with that name in the root folder (it's a feature, not a bug 🐛). 
- If a file with the exact name of a daily note already exists, obsidian will not create a new one from this daily template.
- So to ensure daily-notes are created based on your template, delete any accidentally pre-created files of the same name. 
	- Also, that helps you to keep track 😅

#### prioritize
To focus on what is most relevant for you right now, some kind of task prioritization makes sense. 
Inspired by the Eisenhower matrix, I'm using the Tasks plugin to dynamically distribute all tasks into 4 categories. 
Since this prioritization list can get quite long, I'm [linking to a separate file inside the daily template](plugins/tasks-examples.md#arrange-tasks-into-eisenhower-groups). 




#### journalling

```obsidian
🤗 list placeholder to note what I'm #grateful for today
- 

💩 checkbox placeholder to have fun getting shit done 
- [ ] 
```

#### Google Calendar (advanced)
📢 use plugin "Google Calendar" to include your upcoming events inside the daily note
```gEvent
type: schedule
date: today {{date:YYYY-MM-DD}}  
``` 

##### sample output

- current day highlighted
- past events greyed out

<img src="../pics/google-calendar.png" width="300">

## How to create tasks inside notes?

The tasks plugin converts the following syntax into checkbox items, which can be toggled between todo/done.

`- [ ] ` is displayed as <img src="../pics/checkbox-todo.png">

`- [x] ` is displayed as <img src="../pics/checkbox-done.png">

Hint: Checkbox items include an empty space-character at the end. 

No matter in which note you define a task, it will become part of the dynamic lists shown below - as long as it's marked as `not done`. 
- [ ] a task which is not done has a single empty-space-character inside its checkbox
- [x] a task which is done has a single non-space-character inside its checkbox

<div><img src="../pics/writing-task-done-or-not-done.png" width="600"></div>

To classify tasks you can add parameters
- due date
<div><img src="../pics/due-date.png"></div>
<div><img src="../pics/due-date-parsed.png"></div>
- priority
<div><img src="../pics/task-priority-options.png"></div>

### urgent and important --> do it
```tasks  
not done  

# urgent
due before tomorrow

# important
(priority is high) OR (priority is highest)
```
### urgent but not important --> delegate it
```tasks  
not done  

# urgent
due before tomorrow

# not important
(priority is not high) AND (priority is not highest)
``` 
### important but not urgent --> define it
```tasks  
not done  

# not urgent
due after today
sort by due

# important
(priority is high) OR (priority is highest)
```
### neither important nor urgent --> drop it
```tasks  
not done  

# not urgent
due after today
sort by due

# not important
(priority is not high) AND (priority is not highest)
```  
