[![MIT Licensed][icon-mit]][license]
[![Awesome][icon-awesome]][awesome]
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# Data Structures

# Practice

Remember the http module? Time for practice! Write an application which implements stack and linked list over http.
A consumer of the app may add items to stack or linked list and retrieve items one by one. Stack and linked list may contain only numbers and strings. There should be at least two different endpoints (one for stack, one for linked list), everything else is up to you. Apply your knowledge of http to decide about appropriate http verbs to implement stack/linked list functionality. Decide about the behavior of your app when stack or linked list is empty.
Rememeber: this task may be implemented in many different ways. There is no single correct solution, so try to make the most of this exercise.
No need to use persistent data storage (data base). Save the data in memory.
Describe your API in README.

#### Stack

Operations to be implemented:

- push
- pop

User may add (push) items to the stack and pop item from stack (the stack will no longer contain this item).

```
Push 1
Push 2
Push 3
pop item: 3 will be returned
pop item: 2 will be returned
pop item: 1 will be returned
```

#### Linked list

Operations to be implemented:

- insert
- remove
- show list

User may insert items into the list specifying the successor, remove item from list and see complete list. A request for adding new item will contain the item (mandatory) and item's immediate successor(optional). Item should be inserted before the successor. If no successor is provided, item will be first in the list.

```

Insert C
Insert B before C
Insert A before B

Show all: A - B - C will be returned

Insert Y
Show all: Y - A - B - C will be returned

Remove B
Show all: Y - A - C will be returned

```

1. TBA
1. :vertical_traffic_light:**Node.js**:vertical_traffic_light:
1. :vertical_traffic_light:**Golang**:vertical_traffic_light:

## Done?

➡️ Go forward to [File System](file_system.md)

⤴️ Back to [Contents](../contents.md)

[icon-chat]: https://img.shields.io/badge/chat-on%20telegram-blue.svg
[icon-mit]: https://img.shields.io/badge/license-MIT-blue.svg
[icon-awesome]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
[license]: https://github.com/Kottans/web/blob/master/LICENSE.md
[awesome]: https://github.com/sindresorhus/awesome
