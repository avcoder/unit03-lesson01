---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /assets/intro.jpg
# some information about your slides (markdown enabled)
title: Software Development | Foundations
info: |
  ## Software Development | Foundations
# apply unocss classes to the current slide
class: text-left
drawings:
  persist: false
transition: slide-left
mdc: true
---

# Node.js - part 1/12
Back-End Development
- [ ] Node.js
- [ ] Github

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
TODO: fill in anchor href above to point to github repo for these slides
-->

---
transition: slide-left
---

# Intro to Node.js
(5 min) What is the point of Node.js?

- Node.js is a JS runtime, but does not have access to the browser, window, DOM or anything client-facing
- Node.js is on the server, has access to file system, networking (think terminal command environment)
- Creator Ryan Dahl forked Chrome V8 (watch him present [Node.js circa 2009](https://www.youtube.com/watch?v=jo_B4LTHi3I#t=3m43s))
- Other server languages: Python(1991), Java/PHP/Ruby(1995), C#(2000), Go(2009), Rust(2010)
- Ask ChatGPT: What popular companies use node.js?
- Ask ChatGPT: What software products use node.js?

Node is just ONE of many ways to achieve results.  We'll use node for how popular it is.

<!--
-->

---
transition: slide-left
---

# Installing Node.js and setting up a project
(10 mins)  Create a new Node.js project

- Download/Install [Node.js](https://nodejs.org/en/download) (i.e. or )
   - note: can also install via [nvm](https://www.freecodecamp.org/news/node-version-manager-nvm-install-guide/)
   - LTS = Long Term Support (even numbers 👍; odd numbers 👎)
   - `node -v` `npm -v`
   - [SEMVER](https://devhints.io/semver)
- Set up environment in VS Code, Prettier, ES Lint, npm intellisense, path intellisense, Git Graph, Bracket Pair Colorizer, REST Client
- Browser > Network tab > Disable cache

<!--
- console.log(global)
-->

---
transition: slide-left
---

# Hello World
(30 mins)  Create a "Hello World" response

- Create a basic Node.js script
   - `npm init`

```js
import http from 'http';
  
const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/html');
  res.write('<h1>hello world</h1>');
  res.end();
});

server.listen(3030)
```
- Challenge: A client wants a server that greets users differently based on their request type: "Hello" for `GET`, "Welcome" for `POST`, and "Goodbye" for `DELETE`.  Create a server that checks the HTTP method via `req.method` and respond accordingly on the /greet endpoint (ex: localhost:3030/greet)

<!--
- res.statusCode = 201;
- res.setHeader('Content-Type', 'application/json');
- res.write(JSON.stringify(person));
- Inspect Network tab
-->

---
transition: slide-left
---

# Network and HTTP basics
(10 min) 

- [Network Model](https://www.9tut.com/images/ccna_self_study/TCP_UDP/TCP_UDP.jpg)
- HTTP: Hypertext Transfer Protocol 
   - set of rules servers use to transfer web docs
   - stateless protocol: each request is unique and has no memory of previous requests
   - to fix: http allows sessions / cookies (thus http while stateless is not sessionless)
- HTTP Headers (metadata) are sent with every request/response and sometimes includes:
   - what type of client sent the request
   - how long should content be stored on client
   - what format data is in
- HTTP works on request/response pairs where every request is initiated with an HTTP method and a RESPONSE returns [status code](https://www.restapitutorial.com/httpstatuscodes):

<!--
-->


---
transition: slide-left
---

# Terminology
(10 min)

   - User Agent: app acting on behalf of user (ex: browser, middleware, Google service)
   - TCP: Transmission Control Protocol
   - IP: Internet Protocol
   - DNS: URLs are human readable addresses stored in Domain Name Servers
   - Server: computer on internet that usually runs data storage / web app
   - Cache: way to store data on client/server to speed up perf (ex: CSS may be cached)
   - Cookie: small string of data passed back/forth between client/server to create stateful session
   
---
transition: slide-left
---

# URL structure
(5 min)

- Protocol vs URN (Universal Resource Name)
- URN
   - Host
   - port (usually hidden)
   - resource path (usually file location within server; looks for index.html by default)
   - URL query (`?` separates path from query; uses `&` to connect multiple key/value pairs)
- Query string parameters



---
layout: image-right
transition: slide-left
image: /assets/dahl.png
backgroundSize: 500px 160px
class: text-left
---

# 10 minute break

🍦 Cool Tips, Trends and Resources:

- 📓 [NVM Install Guide](https://www.freecodecamp.org/news/node-version-manager-nvm-install-guide/)
- ▶️ [Node.js Documentary](https://www.youtube.com/watch?v=LB8KwiiUGy0)
- ▶️ [Node Inventor talk: 10 years later](https://www.youtube.com/watch?v=M3BM9TB-8yA)
- 🙏 [HTTP request methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods)
- 📔 [Backend definition](https://techterms.com/definition/backend)
- 🏗️ [Back-End Web Architecture](https://www.codecademy.com/article/back-end-architecture)
- 🪵 [Front-End vs Back-End](https://blog.teamtreehouse.com/i-dont-speak-your-language-frontend-vs-backend)
- 🛞 [Choose an open source license](https://choosealicense.com/)
<br>
<hr>
<br>

- 🧪 [Enter anonymous lab questions](https://docs.google.com/forms/d/e/1FAIpQLSevvGARdHQikso-uLqFCO481MABKE5HofuSrlzEPMNQ2ZLykw/viewform?usp=dialog)
- ℹ️ [Course feedback survey](https://circuitstream.typeform.com/to/ZoyYk7px#course_id=SoftwareAN&instructor=9514)

<!-- 
- take attendance
-->

---
transition: slide-left
---

# Github
(10 mins) Practice pushing commit to GH repo

- Git is not GitHub
- Why is GitHub important?
- Other options: GitLab, BitBucket
- Challenge: commit your code, create Github repo and push your commit

---
transition: slide-left
---

# Command Line Basics
(30 min) Utilize the command line

- What is the command line?  Why is it important to learn how to use it?
- `ls` `cd` `pwd` `mkdir` `cp` `mv` `rm` `touch` `man` `cat` `more` `echo` `grep`
- flags, bash
- operators: `>` `|` `*` `&&`
- Can open applications like VS Code via `vi` or `vim`, `nano`, `code .`
- Challenge: Using only terminal commands:
   - create a new desktop folder called `test`
   - within that folder create a new file called `test.txt` that has the sentence `"Hello World"`
   - create another new file called `README.md` that has a heading and a sentence with a link to google
- `ping` `traceroute` `curl` `wget` `telnet`

<!--
- Show telnet connecting to Live Server
- GET / HTTP/1.1 OR GET /data.js HTTP/1.1
- host:localhost
-->

---
transition: slide-left
---

# Modules & npm
(20 mins) 

- Encapsulation: recall how objects can encapsulate data and functions
- What is `npm`? 
   - [see npmjs.com](npmjs.com)
   - See [npm left-pad incident that broke the internet](https://en.wikipedia.org/wiki/Npm_left-pad_incident)
- How to `npm i`, `node_modules` folder, `package.lock` file, `npm uninstall`
- How to import vs export (commonjs uses require; ES6 uses import)


<!--
- Browser: <script type="module" src="./module.js"></script>
- Node: import { sayHello } from './module.js'; sayHello() 
- package.json: "type": "module",
-->

---
transition: slide-left
---

# Homework

- Learn shell commands by playing: https://web.mit.edu/mprat/Public/web/Terminus/Web/main.html
- Start Freecodecamp ["Managing Packages with NPM"](https://www.freecodecamp.org/learn/back-end-development-and-apis/)
