###
class Diary():
>>> Add to a list /  Return nothing
    def add(self, diary_entry):
    pass

>>> Return a list
    def all(self):
    pass

###
class DiaryEntry():
>>>
    def __init__(self, title, contents):
    pass

###
class TaskList():
>>>
    def add(self, task):
    pass

>>>
    def all_incomplete(self):
    pass

>>>
    def all_complete(self):
    pass

###
class Task():
>>>
    def __init__(self, title):
    pass

>>>
    def mark_complete(self):
    pass

###
class PhoneNumber():
>>>
    def __init__(self, diary):
    pass

>>>
    def extract(self):
    pass

###
class Readable():
>>>
    def __init__(self, diary):
    pass

>>>
    def extract(self, wpm, minutes):
    pass




### ### ### ### ### ### ### ### ### ### ### ### ### ### ### <<<>>> ### ### ### ### ### ### ### ### ### ### ### ### ### ### ###





#             ### Single Test ###            #

### Diary
>>> Initially Diary has no entries:
diary = Diary()
dairy.all() -> []

### DiaryEntry
>>> DiaryEntry is constructed with title and contents
entry = DiaryEntry("My title", "My content")
entry.title -> "My title""
entry.contents -> "My content"

### TaskList
>>> Initially TaskList has no task
task_list = TaskList()
task_list.all() -> []

### Task
>>> Task contructs with title
task = Task("Walk the dog")
task.title -> "Walk the dog"






#             ### Integration Test ###            #

>>> When add multiple diary entries and all list them out the order they were added
diary = Diary()
entry_1 = DiaryEntry("My title 1", "My content 1")
entry_2 = DiaryEntry("My title 2", "My content 2")
entry_3 = DiaryEntry("My title 3", "My content 3")
diary.add(entry_1)
diary.add(entry_2)
diary.add(entry_3)
diary.all() -> [enty_1, entry_2, entry_3]

>>> When I add multiple task and I don't mark any complete #all_incomplete lists them out in the order they were added.
task_list = TaskList()
task_1 = Task("Walk the dog")
task_2 = Task("Walk the cat")
task_3 = Task("Walk the frog")
task_list.add(task_1)
task_list.add(task_2)
task_list.add(task_3)
task_list.all_incomplete() -> [task_1, task_2, task_3]