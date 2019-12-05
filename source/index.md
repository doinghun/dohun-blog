---
layout: page
widgets:
---

{% raw %}

<div class="wrapper">
    <div class="typewriter">
        <h1>
            <a href="" class="typewrite" data-period="2000"
                data-type='[ &quot;Hi, I’m Dohun.&quot;, &quot;I Love to Make Things.&quot;, &quot;I Love Great Design.&quot;, &quot; I Learn Everyday.&quot; ]'>
                <span class="wrap"></span>
            </a>
        </h1>
    </div>
</div>

{% endraw %}

<center>
  {% img '/img/undraw_digital_nomad_9kgl.svg' 300 %}
  <br>
</center>

## Intro.

Hey there, I'm Dohun, Growth Marketer turned Software Developer.
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

## **Projects**

### **Merlabot**

<center>
  {% img '/img/Merlabot_Animation.gif' 200 %}
  <br>
</center>

{% raw %}

  <div class="project-links">
    <a class="button is-large is-white" href="http://bit.ly/2ONZh5E">
      <span class="icon"><i class="fab fa-github"></i></span>
    </a>
    <a class="button is-large is-white" href="http://bit.ly/2RhtBr1">
      <span class="icon"><i class="fas fa-play"></i></span>
    </a>
  </div>
{% endraw %}

Merlabot is a Singapore Travel bot for Korean tourists. It gives recommendations on what to eat in Singapore and answers frequently asked questions about Singapore.

<!-- It is built on Node.js app running on heroku server with Dialogflow API & Facebook Messenger API integration and uses PostgreSQL for databases. -->

Tech Stack:

- `Node.js`
- `PostgreSQL`
- `Dialogflow`

### **ToDo List**

<center>
  {% img '/img/todolist-capture.PNG' 1000 %}
  <br>
</center>

{% raw %}

  <div class="project-links">
    <a class="button is-large is-white" href="http://bit.ly/2ONoDkk">
      <span class="icon"><i class="fab fa-github"></i></span>
    </a>
    <a class="button is-large is-white" href="http://bit.ly/34IVdsZ">
      <span class="icon"><i class="fas fa-play"></i></span>
    </a>
  </div>
{% endraw %}

This is a simple todo list made with nodejs & ejs template engine. It also includes authentication with sign-up & login and database to save user info as well as their todo task lists.

Tech Stack:

- `Node.js`
- `EJS`
- `PostgreSQL`
- `Axios`

### **Instagram Like Bot**

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

I built Instagram Like bot with puppeteer web-scraping library that automatically likes the top 3 recent posts of hashtags provided.

Tech Stack:

- `Node.js`
- `Puppeteer`

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
.wrapper {
  display: flex;
  justify-content: center;
}

.typewriter h1 span{
  color: #000000;
  font-size: 33px;
  font-family: inherit;
  overflow: hidden; /* Ensures the content is not revealed until the animation */
  border-right: .15em solid orange; /* The typwriter cursor */
  white-space: nowrap; /* Keeps the content on a single line */
  margin: 0 auto; /* Gives that scrolling effect as the typing happens */
  letter-spacing: 0em; /* Adjust as needed */
  animation: 
    typing 2s steps(30, end),
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

<script>
var TxtType = function(el, toRotate, period) {
        this.toRotate = toRotate;
        this.el = el;
        this.loopNum = 0;
        this.period = parseInt(period, 10) || 2000;
        this.txt = '';
        this.tick();
        this.isDeleting = false;
    };

    TxtType.prototype.tick = function() {
        var i = this.loopNum % this.toRotate.length;
        var fullTxt = this.toRotate[i];

        if (this.isDeleting) {
        this.txt = fullTxt.substring(0, this.txt.length - 1);
        } else {
        this.txt = fullTxt.substring(0, this.txt.length + 1);
        }

        this.el.innerHTML = '<span class="wrap">'+this.txt+'</span>';

        var that = this;
        var delta = 200 - Math.random() * 100;

        if (this.isDeleting) { delta /= 2; }

        if (!this.isDeleting && this.txt === fullTxt) {
        delta = this.period;
        this.isDeleting = true;
        } else if (this.isDeleting && this.txt === '') {
        this.isDeleting = false;
        this.loopNum++;
        delta = 500;
        }

        setTimeout(function() {
        that.tick();
        }, delta);
    };

    window.onload = function() {
        var elements = document.getElementsByClassName('typewrite');
        for (var i=0; i<elements.length; i++) {
            var toRotate = elements[i].getAttribute('data-type');
            var period = elements[i].getAttribute('data-period');
            console.log(toRotate)
            if (toRotate) {
              new TxtType(elements[i], JSON.parse(toRotate), period);
            }
        }
    };
</script>

{% endraw %}
