The tasks array is the single source of truth, plus one small piece of UI-only state, editingId, that tracks which 
task (if any) is mid-edit. Every mutation — add, toggle, delete, save — changes this state first and then calls one 
render() function, which clears #task-list and rebuilds it from scratch using createElement/appendChild rather than 
patching individual nodes. Because buildTaskElement checks task.id === editingId on every render, a task's row
 automatically switches between its normal view and its inline edit form based purely on that state, with no 
separate DOM-tracking logic needed. The counter and due-date badges are computed the same way, straight from tasks 
each time, so nothing can drift out of sync — the tradeoff is re-rendering more than strictly necessary, which is
 fine at this scale but wouldn't be for a huge list.