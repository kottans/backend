[![MIT Licensed][icon-mit]][license]
[![Awesome][icon-awesome]][awesome]
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# Program in Memory

1. [Anatomy of a Program in Memory](https://manybutfinite.com/post/anatomy-of-a-program-in-memory/)
1. Discover memory mapping on real-life example:
   - Linux systems has pseudo-files system called `proc` which can be used to get extended info about running processes.
   - Use `man proc` shell command to get more info about `proc` or read the same info [here](http://man7.org/linux/man-pages/man5/proc.5.html)
   - If you're Mac user consider to use `vmmap` or `vmmap64` to discover process memory mapping. More info [here](https://developer.apple.com/library/archive/documentation/Performance/Conceptual/ManagingMemory/Articles/VMPages.html#//apple_ref/doc/uid/20001985-97196-TPXREF127).
1. :vertical_traffic_light:**Node.js**:vertical_traffic_light: [Understanding Garbage Collection and Hunting Memory Leaks in Node.js](https://blog.codeship.com/understanding-garbage-collection-in-node-js/)
1. :vertical_traffic_light:**Golang**:vertical_traffic_light: [Go Memory Management](https://povilasv.me/go-memory-management/)

Finish the subtasks (1), (2) and (3) above.

When complete do the following:

1. In your `kottans-backend` repo `README.md`:
   - add header `## Memory Management`
   - add answers to the following questions:
     - What's going to happen if program reaches maximum limit of stack ?
     - What's going to happen if program requests a big (more then 128KB) memory allocation on heap ?
     - What's the difference between Text and Data memory segments ?
1. From your termianl list all currently running processes using `ps -a` command and then:
   - Pick any process you like to check its memory mapping (for instance it can be `bash` process itself) and copy its PID (process ID).
   - Call `cat /proc/<PID>/map` to get info about process memory mapping state. Or `vmmap -64 -p <PID>` on MAC.
   - You will get output with allocated memory map. Discover this info to find _Memory Mapping Segment_, _Heap_ and _Stack_ fragments.
   - Copy output of `proc`/`vmmap` command. And paste it to `kottans-backend` `README.md` file after your `## Memory Management` answers. Use `{content}` Markdown formatting to keep it readable. It should look similar to this:
   ```md
   556dfe5af000-556dfe6b3000 r-xp 00000000 08:08 6553607 /bin/bash
   556dfe8b2000-556dfe8b6000 r--p 00103000 08:08 6553607 /bin/bash
   556dfe8b6000-556dfe8bf000 rw-p 00107000 08:08 6553607 /bin/bash
   556dfe8bf000-556dfe8c9000 rw-p 00000000 00:00 0
   556dff36b000-556dff4e3000 rw-p 00000000 00:00 0 [heap]
   7f558b397000-7f558b3a2000 r-xp 00000000 08:08 1577916 /lib/x86_64-linux-gnu/libnss_files-2.27.so
   7f558b5a3000-7f558b5a9000 rw-p 00000000 00:00 0
   7f558b7c1000-7f558b7c3000 rw-p 00000000 00:00 0
   7f558bbd9000-7f558c720000 r--p 00000000 08:08 3939013 /usr/lib/locale/locale-archive
   7f558c720000-7f558c907000 r-xp 00000000 08:08 1577826 /lib/x86_64-linux-gnu/libc-2.27.so
   7f558cb0d000-7f558cb11000 rw-p 00000000 00:00 0
   7f558cb11000-7f558cb14000 r-xp 00000000 08:08 1577849 /lib/x86_64-linux-gnu/libdl-2.27.so
   7f558cb14000-7f558cd13000 ---p 00003000 08:08 1577849 /lib/x86_64-linux-gnu/libdl-2.27.so
   7f558cf3f000-7f558cf66000 r-xp 00000000 08:08 1577798 /lib/x86_64-linux-gnu/ld-2.27.so
   7f558d148000-7f558d14d000 rw-p 00000000 00:00 0
   7f558d15f000-7f558d166000 r--s 00000000 08:08 4196801 /usr/lib/x86_64-linux-gnu/gconv/modules.cache
   7f558d166000-7f558d167000 r--p 00027000 08:08 1577798 /lib/x86_64-linux-gnu/ld-2.27.so
   7f558d167000-7f558d168000 rw-p 00028000 08:08 1577798 /lib/x86_64-linux-gnu/ld-2.27.so
   7f558d168000-7f558d169000 rw-p 00000000 00:00 0
   7ffe96b2c000-7ffe96b4d000 rw-p 00000000 00:00 0 [stack]
   7ffe96b70000-7ffe96b73000 r--p 00000000 00:00 0 [vvar]
   7ffe96b73000-7ffe96b75000 r-xp 00000000 00:00 0 [vdso]
   ffffffffff600000-ffffffffff601000 r-xp 00000000 00:00 0 [vsyscall]
   ```
   - After `proc/map` output provide examples of _Memory Mapping Segment_, _Heap_ and _Stack_ fragments address. For instance: `Heap - 556dff36b000-556dff4e3000`, `Stack - 7ffe96b2c000-7ffe96b4d000`, `MMS - 7f558b397000-7f558b3a2000`.
1. In your `kottans-backend` repo `README.md` list your reflections on all subtasks
   (_what was new to you_, _what surprised you_, _what you intend to use in future_)
1. You did a lot already! If you honestly finished all the previous steps then go ahead
   and share it with others – post a message in [course channel](https://t.me/joinchat/Dqrdixe1c2K9bXUFBzNWtg):
   `kottans-backend — #done` (or `kottans-backend — #p2p_done` if you are p2p course student) and add the link to your repo. **This step is important, as it helps mentors to track your progress!**
1. Study Extra Materials below to improve your skills.
   If you feel it affects your overall course performance consider
   reverting to those later e.g. when you have all mandatory tasks completed.
1. You may skip Optional materials from this task (if any).

When you finish this task you can proceed to the next one.

## Extra materials

- :vertical_traffic_light:**Node.js**:vertical_traffic_light: [Accessing Node.js Memory Using V8 Inspector & Chrome Dev Tools](https://marmelab.com/blog/2018/04/03/how-to-track-and-fix-memory-leak-with-nodejs.html#accessing-nodejs-memory-using-v8-inspector--chrome-dev-tools)
- :vertical_traffic_light:**Node.js**:vertical_traffic_light: [Node.js Garbage Collection Explained](https://blog.risingstack.com/node-js-at-scale-node-js-garbage-collection/)
- :vertical_traffic_light:**Golang**:vertical_traffic_light: [Debugging: Simple Memory Leaks in Go](https://medium.com/dm03514-tech-blog/sre-debugging-simple-memory-leaks-in-go-e0a9e6d63d4d)
- :vertical_traffic_light:**Golang**:vertical_traffic_light: [Avoiding Memory Leak in Golang API](https://hackernoon.com/avoiding-memory-leak-in-golang-api-1843ef45fca8)

## Done?

➡️ Go forward to [TCP. UDP. Network](network.md)

⤴️ Back to [Contents](../contents.md)

[icon-chat]: https://img.shields.io/badge/chat-on%20telegram-blue.svg
[icon-mit]: https://img.shields.io/badge/license-MIT-blue.svg
[icon-awesome]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
[license]: https://github.com/Kottans/web/blob/master/LICENSE.md
[awesome]: https://github.com/sindresorhus/awesome#front-end-development
[node]: ../img/node.png
[go]: ../img/go.png
