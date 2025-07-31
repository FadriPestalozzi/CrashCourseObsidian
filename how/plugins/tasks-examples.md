# Why use [Tasks](https://publish.obsidian.md/tasks/Reference/Task+Formats/About+Task+Formats)?

A key role of Obsidian as your second brain is it's ability to deal with messy input data. 
That's where the Tasks-plugin shines 😄

Whenever I think about a task, I just write it into whatever note I am currently working on. 
Afterwards, I can then review all open tasks from all notes inside of my Obsidian vault by checking Eisenhower-style lists (see below). 

## sample input
- this shows the syntax to create tasks 
- tasks can be defined in any note within your vault

- [ ] an open task without prioritization
- [x] a closed task without prioritization ✅ 2025-07-30
- [ ] a high priority task due in the past 📅 2025-07-22 ⏫ 
- [x] another high priority task due in the past which is already done ⏫ 📅 2025-07-22 ✅ 2025-07-30
- [ ] a high priority task due in the future ⏫ 📅 2025-07-31
- [ ] a low priority task due in the past 📅 2025-07-22 🔽 
- [ ] a low priority task due in the future 📅 2025-07-31 🔽 

## sample output 
- output generated on 2025-07-30

![](../../pics/Pasted image 20250730002216.png)

# arrange tasks into Eisenhower groups
## urgent and important --> do it
```tasks  
not done  

# urgent
due before tomorrow

# important
priority is high 
```

### sample output

![](../../pics/Pasted image 20250730230643.png)

## urgent but not important --> delegate it
```tasks  
not done  

# urgent
due before tomorrow

# not important
priority is not high 
``` 

### sample output

![](../../pics/Pasted image 20250730230703.png)

## important but not urgent --> define it
```tasks  
not done  

# not urgent
due after today
sort by due

# important
(priority is high) OR (priority is highest)
```

## neither important nor urgent --> drop it
```tasks  
not done  
due after today  
sort by due
short mode  

# not important
priority is not high 
```  

## option to hide edit button and backlinks
```tasks  
not done  
due after today  
sort by due
short mode  

# not important
priority is not high 

hide edit button  
hide backlink  
```  


### sample output

![](../../pics/Pasted image 20250730230729.png)