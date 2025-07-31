The [Dataview plugin](https://github.com/blacksmithgu/obsidian-dataview) allows you to treat your Obsidian Vault as a database which you can query. 
This includes powerful features like filtering, sorting, and extracting data from Markdown pages.

Apart from the examples shown on the [plugin repo](https://github.com/blacksmithgu/obsidian-dataview?tab=readme-ov-file#examples), I'm using this plugin for customized file searches. 

# customized file search

## sample code input

The example below implements several dataview features.
1. list files in table with second column = modification date
	- `TABLE dateformat(file.mtime, "dd.MM.yyyy - HH:mm")`
2. search in target folder
	- `FROM "0-todo"`
3. list up to 3 files
	- `limit 3`
4. sorted by modification date in descending order (latest first)
	- `sort file.mtime desc`

```dataview 
TABLE dateformat(file.mtime, "dd.MM.yyyy - HH:mm") AS "Last modified"
FROM "0-todo"
sort file.mtime desc
limit 3
```

## sample output

![](../../pics/Pasted image 20250730083812.png)

### option to hide specific file
5. adding a filter to hide the file `0-todo.md`
	- `WHERE file.name != "0-todo"`

```dataview 
TABLE dateformat(file.mtime, "dd.MM.yyyy - HH:mm") AS "Last modified"
FROM "0-todo"
WHERE file.name != "0-todo"
sort file.mtime desc
limit 3
```

![](../../pics/Pasted image 20250730083752.png)



### include entire path from vault root

In case your target folder is nested within other folder(s), indicate the entire path starting from your vault root.
- `FROM "network/personal/family/awoken_machines"`

```dataview 
TABLE dateformat(file.mtime, "dd.MM.yyyy - HH:mm") AS "Last modified"
FROM "network/personal/family/awoken_machines"
WHERE file.name != "awoken_machines"
sort file.mtime desc
limit 5
```

#### each folder nesting level is indicated by vertical line

![](../../pics/Pasted image 20250730085944.png)