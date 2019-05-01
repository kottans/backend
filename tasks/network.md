[![MIT Licensed][icon-mit]][license]
[![Awesome][icon-awesome]][awesome]
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# TCP. UDP. Network

1. [Internet 101](https://www.khanacademy.org/computing/computer-science/internet-intro)
1. [Networking for Web Developers](https://www.udacity.com/course/networking-for-web-developers--ud256)
1. [How DNS Works](https://howdns.works/)
2. :vertical_traffic_light:__Node.js__:vertical_traffic_light:[TCP client in Node.js](https://riptutorial.com/node-js/example/22406/a-simple-tcp-client):vertical_traffic_light:__Node.js__:vertical_traffic_light:
3. :vertical_traffic_light:__Python__:vertical_traffic_light:[TCP echo client in Python][TCP Communication](https://wiki.python.org/moin/TcpCommunication):vertical_traffic_light:__Python__:vertical_traffic_light:
4. :vertical_traffic_light:__Golang__:vertical_traffic_light:[TCP client and server in Golang](https://systembash.com/a-simple-go-tcp-server-and-tcp-client/):vertical_traffic_light:__Golang__:vertical_traffic_light:


Finish the courses (1), and (2) and read article (3) above.  
1. Make screenshots of your finished lessons from (1), (2)
   and put the screenshots in `task_networks` folder in
   your `kottans-backend` repo
2. In your `kottans-backend` repo `README.md`:
   * add header `## TCP. UDP. Network`
   * embed the screenshots or add links to the screenshots
   * list your reflections on all subtasks
     (_what was new to you_, _what surprised you_, _what you intend to use in future_)
3. In your `task_networks` folder build a following program:
  ### TCP Port Sniffer :nose:
  Sniffer is [CLI](https://en.wikipedia.org/wiki/Command-line_interface) tool which allows user to easily search for opened TCP ports on particular host (using IP adderess or domain). Example of usage:

  :vertical_traffic_light:__Node.js__:vertical_traffic_light:

  `node sniffer.js --ports 10-9999 --host 172.217.3.110`

  `....`
  
  `22,54,80,443 ports are opened`

  :vertical_traffic_light:__Node.js__:vertical_traffic_light:

  :vertical_traffic_light:__Golang__:vertical_traffic_light:

  `go run sniffer.go --ports 10-9999 --host 172.217.3.110`

  `....`
  
  `22,54,80,443 ports are opened`

  :vertical_traffic_light:__Golang__:vertical_traffic_light:

  :vertical_traffic_light:__Python__:vertical_traffic_light:

  `python sniffer.py --ports 10-9999 --host 172.217.3.110`

  `....`
  
  `22,54,80,443 ports are opened`

  :vertical_traffic_light:__Python__:vertical_traffic_light:

  ##### TCP sniffer user stories

  * As the user, I can call sniffer from by shell with one required argument `--host` which can be either domain name, like `google.com` or IP address like `172.217.3.110`.
  * After call program will start TCP ports scan, trying to dial each port from `0`to `65535`. If dial is successful program will print dot `.` to `stdout` and save found open port to buffer array. **IMPORTANT**: Each dial attempt should have `300ms` timeout. (If client fails to connect in `300ms` port is skipped).
  * After scan is finished program will print the list of opened ports to `stdout` and exit with status code `0`.
  * As the user, I can limit the range of ports to scan by providing `--ports` argument in format `<start_port>-<end_port>`, for instance: `3-600`.
  * As the user, I can get a descriptive error if required argument are missing or if some of them have incorrect format.
  * As the user, I can provide `--help` flag to see hint about how to use `TCP sniffer`.


4. You did lot already! If you honestly finished all the previous steps then go ahead
   and share it with others –
   post a message in [course channel][chat]:
   `TCP. UDP. Network — #done` (or `TCP. UDP. Network — #done` if you are p2p course student) and add the link to your repo. **This step is important, as it helps mentors to track your progress!** 
When complete do the following:

## Extra materials
1. [Introduction to TCP/IP. Course](https://www.coursera.org/learn/tcpip)
1. [What happens when you type google.com into your browser and press enter?](https://github.com/alex/what-happens-when)
2. [Big list of TCP/UDP ports](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)
4. :vertical_traffic_light:__Node.js__:vertical_traffic_light:[Module 'net' Node.js docs](https://nodejs.org/api/net.html):vertical_traffic_light:__Node.js__:vertical_traffic_light:
5. :vertical_traffic_light:__Golang__:vertical_traffic_light:[Package 'net' Golang docs](https://golang.org/pkg/net/):vertical_traffic_light:__Golang__:vertical_traffic_light:
6. :vertical_traffic_light:__Python__:vertical_traffic_light:[TCP echo client in Python](https://pymotw.com/2/socket/tcp.html#echo-client):vertical_traffic_light:__Python__:vertical_traffic_light:


## Done?

➡️ Go forward to ...

⤴️ Back to [Contents](../contents.md)

[icon-chat]: https://img.shields.io/badge/chat-on%20telegram-blue.svg
[icon-mit]: https://img.shields.io/badge/license-MIT-blue.svg
[icon-awesome]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
[license]: https://github.com/Kottans/web/blob/master/LICENSE.md
[awesome]: https://github.com/sindresorhus/awesome
