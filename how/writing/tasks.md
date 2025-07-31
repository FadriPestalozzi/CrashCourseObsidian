# How to create tasks inside notes?

## checkbox items

The tasks plugin converts the following syntax into checkbox items, which can be toggled between `not done` and `done`.

- `not done` checkbox
    - starting a line with `- [ ] `
    - displayed as <img src="../../pics/checkbox-todo.png">

- `done` checkbox 
    - starting a line with `- [x] `
    - displayed as <img src="../../pics/checkbox-done.png">

Hint: Checkbox items must include an empty space-character at the end. 

## done vs. not done

No matter in which note you define a task, it will become part of the dynamic lists shown <a href="../plugins/tasks-examples.md#arrange-tasks-into-eisenhower-groups">here</a> - as long as it's marked as `not done`. 


- [ ] a task which is not done has a single empty-space-character inside its checkbox
- [x] a task which is done has a single non-space-character inside its checkbox

### sample output

<div><img src="../../pics/writing-task-done-or-not-done.png" width="600"></div>


## classify tasks

To classify tasks you can add the parameters `due date` and `priority`

### due date

<div><img src="../../pics/due-date.png"></div>

<div><img src="../../pics/due-date-parsed.png"></div>

### priority

<div><img src="../../pics/task-priority-options.png"></div>

