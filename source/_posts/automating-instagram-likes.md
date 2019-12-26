---
title: Automating Instagram Likes
layout: page
widgets:
category: Projects
thumbnail: /2019/12/10/automating-instagram-likes/like-machine.png
---

- Programme that automates Instagram likes for Instagram account growth.

<!--more-->
<center>
  {% img '/img/ig-bot-demo.gif' 600 %}
  <br>
</center>
{% raw %}

  <div class="project-links">
    <a class="button is-large is-white" href="http://bit.ly/36bl6SL">
      <span class="icon"><i class="fab fa-github"></i></span>
    </a>
  </div>
{% endraw %}

### Built with 🏗️

---

- Express.js (Node.js)
- Puppeteer

### Features 👀

---

- Likes top 3 recent posts of hashtags provided

### Setup 🚀

---

- clone, navigate to the root directory, and `npm install`
- Create `config.js` file with `IG_ID` & `IG_PW` values
- Create `tags.js` file with IG hashtags in array
- Run program using `npm start`
