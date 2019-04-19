[![MIT Licensed][icon-mit]][license]
[![Awesome][icon-awesome]][awesome]
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# File System

In this section we will dive into the basics of Unix based file systems. Particularly, you will discover
notions of file descriptors, users / groups access permissions, special files etc.

## Theory

1. Read about [typical file system structure in Unix Systems](https://www.geeksforgeeks.org/operating-system-unix-file-system/)
1. Discover [unix file permissions and access modes](https://www.tutorialspoint.com/unix/unix-file-permission.htm)
1. :vertical_traffic_light:**Node.js**:vertical_traffic_light: [Node.js File System](https://www.tutorialsteacher.com/nodejs/nodejs-file-system)
1. :vertical_traffic_light:**Golang**:vertical_traffic_light: [Working with Files in Go](https://www.devdungeon.com/content/working-files-go)

## Practical Task

1. Create folder called `file_system` folder in
   your `kottans-backend` repo
1. In `file_system` folder:
   - create file called `secret.txt`
   - grant read-write-execute permissions to owned user, read-only permission to owned group and no permissions to other users for file `secret.txt`. Permission indicator for this file should be: `-rwxr-----`
   - commit and push your changes to remote
1. :vertical_traffic_light:**Node.js**:vertical_traffic_light: In your `kottans-backend` folder create file `file_system_task.js`. In this file, implement a program with following behavior:
   - Upon run (with `node file_system_task.js`), program checks whether or not file `counter.txt` exists.
   - _If its not_. Program creates new file `counter.txt` with write/read/execute access to **all** users. Then it writes single digit `1` into the file, closes it and exists with status code 0 (normal exit).
   - _If it does exist_. Program opens the file `counter.txt`, reads its content and checks whether or not all the content of the file is valid **integer**. If its valid integer, program increments counter by one, writes new digit into the file (replaces previous one), closes the file and exists with status code 0 (normal exit). If its not valid immediately exists with status code 1 (abnormal exit).
1. :vertical_traffic_light:**Golang**:vertical_traffic_light: In your `kottans-backend` folder create file `file_system_task.go`. Within this file, implement program with following behavior:
   - Upon run (with `go run file_system_task.go`, consider that your `file_system_task.go` should have `main` function to be executable), program checks whether or not file `counter.txt` exists.
   - _If its not_. Program creates new file `counter.txt` with write/read/execute access to **all** users. Writes single digit `1` into the file, closes it and exists with status code 0 (normal exit).
   - _If it does exist_. Program opens the file `counter.txt`, reads its content and checks whether or not all the content of the file is valid **integer**. If its valid integer, program increments counter by one, writes new digit into the file (replaces previous one), closes the file and exists with status code 0 (normal exit). If its not valid immediately exists with status code 1 (abnormal exit).
1. In your `kottans-backend` repo `README.md`:
   - add header `## File System`
   - embed the links to your `secret.txt` file and `file_system_task` source code file.
1. You did lot already! If you honestly finished all the previous steps then go ahead
   and share it with others –
   post a message in [course channel][chat]:
   `File System — #done` and add the link to your repo. **This step is important, as it helps mentors to track your progress!**

## Extra materials

1. :vertical_traffic_light:**Node.js**:vertical_traffic_light: Node.js docs on `fs` [module](https://nodejs.org/api/fs.html)
2. :vertical_traffic_light:**Golang**:vertical_traffic_light: Reading files in various use cases. [Golang tutorial series. No. 35](https://golangbot.com/read-files/).
3. :vertical_traffic_light:**Node.js**:vertical_traffic_light: [Руководство по Node.js, часть 9: работа с файловой системой](https://habr.com/ru/company/ruvds/blog/424969/)

## Done?

➡️ Go forward to ...

⤴️ Back to [Contents](../contents.md)

[chat]: https://tbd.com
[icon-chat]: https://img.shields.io/badge/chat-on%20telegram-blue.svg
[icon-mit]: https://img.shields.io/badge/license-MIT-blue.svg
[icon-awesome]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
[license]: https://github.com/Kottans/web/blob/master/LICENSE.md
[awesome]: https://github.com/sindresorhus/awesome
