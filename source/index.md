---
layout: about
title: About Me
date: 2019-10-07 20:24:29
widgets:
  - type: recent_posts
    position: right
---

{% raw %}

<div class="typewriter">
  <h1>Hi, I'm Dohun.</h1>
</div>

{% endraw %}

<center>
  {% img '/img/me.jpg' 300 %}
  <br>
</center>

## Intro.

Hey there, I'm Dohun, Growth Marketer turned Developer.
Currently living in Singapore 🇸🇬.

{% raw %}

<div id="contact-buttons" class="buttons is-centered">
  <a class="button is-dark is-medium" href="https://github.com/doinghun">
    <span class="icon"><i class="fab fa-github"></i></span>
    <span>Github</span>
  </a>
  <a class="button is-linkedin is-medium" href="https://www.linkedin.com/in/dohunkim1/">
    <span class="icon"><i class="fab fa-linkedin"></i></span>
    <span>LinkedIn</span>
  </a>
  <a class="button is-light is-medium" href="mailto:de.qtner@gmail.com">
    <span class="icon"><i class="far fa-envelope"></i></span>
    <span>Email</span>
  </a>
</div>
{% endraw %}

---

{% raw %}

<style>
.buttons {
  width: 100%;
  display: flex;
}
.buttons a.button {
  flex-grow: 1;
}
a.button.is-linkedin {
  background-color: #0077B5;
  border-color: #0077B5;
  color: #FFF;
}
@media screen and (max-width: 720px) {
  .buttons a.button {
    width: 100%;
    margin-right: 0;
  }
}
.project-links {
  margin-bottom: 16px;
}

/* DEMO-SPECIFIC STYLES */
.typewriter h1 {
  text-align: center;
  color: #000000;
  font-family: roboto;
  overflow: hidden; /* Ensures the content is not revealed until the animation */
  border-right: .15em solid orange; /* The typwriter cursor */
  white-space: nowrap; /* Keeps the content on a single line */
  margin: 0 auto; /* Gives that scrolling effect as the typing happens */
  letter-spacing: 0em; /* Adjust as needed */
  animation: 
    typing 3.5s steps(30, end),
    blink-caret .5s step-end;
}

/* The typing effect */
@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}

/* The typewriter cursor effect */
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: orange }
}
</style>

{% endraw %}
