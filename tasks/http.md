[![MIT Licensed][icon-mit]][license]
[![Awesome][icon-awesome]][awesome]
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# Http & Https


1. Reading: [HTTP: The Protocol Every Web Developer Must Know - Part 1](https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)
1. Reading: [HTTP: The Protocol Every Web Developer Must Know - Part 2](https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-2--net-31155)
1. Tutorial: ["How HTTPS Works"](https://howhttps.works/)
1. Reading: ["Public-key Cryptography for Non-geeks"](https://blog.vrypan.net/2013/08/28/public-key-cryptography-for-non-geeks/)
1. Reading: ["How HTTPS Actually Works"](https://robertheaton.com/2014/03/27/how-does-https-actually-work/)


## Practice

This task is based to [this](https://gist.github.com/btoone/2288960) tutorial by [Brandon Toone](https://github.com/btoone).
It's time to apply your knowledge about http by writing actual requests. For this we will use popular commad-line tool `cURL`. Please find out how to install this tool on your OS.  
We will explore GitHub API. GitHub provides JSON-based API where you can get various informations about users, repositories, commits etc.
For better learning experience we suggest that you type the requests yourself instead of copy-pasting them.
Let's start by getting information about you:

```bash
curl https://api.github.com/users/<YOUR GitHub NAME>
```

Add `-i` flag, which stands for "include", to see the headers received from server. Find information about unknown headers.

```bash
curl -i https://api.github.com/users/<YOUR GitHub NAME>
```

Let's access a resource which requires authentication. We will request the list of gists user has starred. First, try to access it without credentials and see the result.
```bash
curl  https://api.github.com/gists/starred
```
 `--user` parameter in curl is used for server authentication. You can add user name and password to the request after this parameter. Let's try to use invalid credentials and see the result first. Replace "USERNAME" with your actual GitHub user name.

```bash
curl --user "USERNAME:BLABLABLA" https://api.github.com/gists/starred
```

Now, try the request with correct credentials. By the way, the authentication scheme is called "Basic" (credentials are provided in (every) request directly). Replace "USERNAME" and "PASSWORD" with your actual GitHub user name and password.

```bash
curl --user "USERNAME:PASSWORD" https://api.github.com/gists/starred
```

You can also try to add your user name only.
```bash
curl --user "USERNAME" https://api.github.com/gists/starred
```
In this case you will be prompted to enter your password. This way you will avoid getting your password into command line history.

Additional tasks:
- list repositories of "Kottans" organization. For this task you need to explore GitHub API documentation: https://developer.github.com/v3/guides/getting-started/#repositories
- Create new issue in your repository

Write down all your requests (replace sensitive information like password with "*" symbols)in the repository.

## Questions

Add answers to the following questions to your repository:
1. Name at least three possible negative consequences of not using https.
1. Explain the main idea behind public key cryptography in few sentences
1. You are creating an application for pet clinic. You need to implement the following functionality:
- add new pet (including name, age, breed, owner's name, medical history)
- search pet by name
- change name of an existing pet
- add new info about pet's health
- assign a pet to a particular doctor in the clinic
- register an appointment for a pet. This request should include info about pet, doctor and appointment date and time.  

Choose http verbs for every piece of functionality. If applicable, describe also the way you would provide data to the request (vie query params, in request body etc.). If applicable, describe the response of the server. Explain your choice.

## Extra Materials

1. Reading: ["HTTPS In the Real World"](https://robertheaton.com/2018/11/28/https-in-the-real-world/)
1. Reading: ["How SSL/TLS Works"](https://certs.securetrust.com/support/support-how-ssl-works.php)

## Done?

➡️ Go forward to [Design Patterns: Intro](patterns.md)

⤴️ Back to [Contents](../contents.md)

[icon-chat]: https://img.shields.io/badge/chat-on%20telegram-blue.svg
[icon-mit]: https://img.shields.io/badge/license-MIT-blue.svg
[icon-awesome]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
[license]: https://github.com/Kottans/web/blob/master/LICENSE.md
[awesome]: https://github.com/sindresorhus/awesome
