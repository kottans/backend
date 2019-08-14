[![MIT Licensed][icon-mit]][license]
[![Awesome][icon-awesome]][awesome]
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# Data Structures


# Practice

Remember the http module? Time for practice! Write an application which implements stack and queue with access over http.
A consumer of the app may add items to stack or queue and retrieve items one by one. Stack and queue may contain only numbers and strings. There should be at least two different endpoints (one for stack, one for queue), everything else is up to you. Apply your knowledge of http to decide about appropriate http verbs to implement stack/queue functionality. Decide about the behavior of your app when stack or queue is empty.
Rememeber: this task may be implemented in many different ways. There is no single correct solution, so try to make the most of this exercise.
No need to use persistent data storage (data base). Save the data in memory.
Describe your API in README.

#### Example requests:
Stack:
```
Add 1
Add 2
Add 3
get item: 3 will be returned
get another item: 2 will be returned
get another item: 1 will be returned
```

Queue:
```
Add 'a'
Add 'b'
Add 'c'
get item: 'a' will be returned
get another item: 'b' will be returned
get another item: 'c' will be returned
```

1. TBA
1. :vertical_traffic_light:__Node.js__:vertical_traffic_light:
1. :vertical_traffic_light:__Golang__:vertical_traffic_light:

## Done?

➡️ Go forward to ...

⤴️ Back to [Contents](../contents.md)

[icon-chat]: https://img.shields.io/badge/chat-on%20telegram-blue.svg
[icon-mit]: https://img.shields.io/badge/license-MIT-blue.svg
[icon-awesome]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
[license]: https://github.com/Kottans/web/blob/master/LICENSE.md
[awesome]: https://github.com/sindresorhus/awesome
