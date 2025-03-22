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

# Recap
(10 min) 

- Refresher about JS syntax, variables, objects, console
- Examine Network tab/Postman for network requests 
   - see Header, Payload, Response
   - What kind of responses do we get?  
- [Network Model](https://www.9tut.com/images/ccna_self_study/TCP_UDP/TCP_UDP.jpg)

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
-->

---
transition: slide-left
---

# Intro to Node.js
(20 min) What is the point of Node.js?

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

# Installing Node.js and setting up a project
(20 mins)  Create a new Node.js project

- Download/Install Node.js 
   - note: can also install via `nvm`
   - LTS = Long Term Support (even numbers 👍; odd numbers 👎)
   - `node -v` `npm -v`
   - [SEMVER](https://devhints.io/semver)
- Set up environment in VS Code, Prettier, ES Lint, npm intellisense, path intellisense, GitLens, Bracket Pair Colorizer
- Browser > Network tab > Disable cache
- Create a Node.js project

<!--
-->


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
- ▶️ [Node.js Documentary]
- ▶️ [10 Things I regret about node.js](https://www.youtube.com/watch?v=M3BM9TB-8yA)

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

# Hello World
(20 mins)  Create a "Hello World" response

- Create a basic Node.js script
- Challenge: console.log('Hello World') to the terminal
- Challenge: Server respond with `<h1>Hello World</h1>`/JSON (test response with browser)

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

<!--
- res.statusCode = 201;
- res.setHeader('Content-Type', 'application/json');
- res.write(JSON.stringify(person));
- Inspect Network tab
-->

---
transition: slide-left
---

# Modules & npm
(30 mins) 

- Encapsulation: recall how objects can encapsulate data and functions
- Modules in node.js via `require()` or `import`
- `node_modules` folder
- What is `npm`? 
   - [see npmjs.com](npmjs.com)
   - See [npm left-pad incident that broke the internet](https://en.wikipedia.org/wiki/Npm_left-pad_incident)

---
transition: slide-left
---

# Github
(10 mins) What is GitHub?

- Git is not GitHub
- Why is GitHub important?
- Other options: GitLab, BitBucket
- Did you know?  You can use GitHub as your public-facing portfolio?
- Challenge: commit your code, create Github repo and push your commit

---
transition: slide-left
---

# Homework

- Goto: https://www.freecodecamp.org/learn/back-end-development-and-apis/
- Start Freecodecamp "Managing Packages with NPM" followed by "Basic Node and Express"
- Continue as far as you can
