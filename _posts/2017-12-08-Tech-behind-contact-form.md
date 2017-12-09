---
layout: post
title: Tech Behind Contact Form
description: >
 Today , i'm going to tell you how i created this lovely [contact form](/contact).
---
<!--more-->
## Table of Contents
{:.no_toc}
- TOC
{:toc}



## Introduction

Today , i'm going to tell you how i created this lovely [contact form](/contact). You can easily check it's source code through any online source code checker or by pressing CTRL+U (pc users). However, i mostly use w3 to inspect the source code.

Online source code is here: 

1.[w3.org](https://validator.w3.org/nu/?showsource=yes&showimagereport=yes&doc=https%3A%2F%2Fcontact.sirkapil.me%2F)

2.[Raw Github](https://raw.githubusercontent.com/sirkapil/contact/gh-pages/index.html)

Can't find the form code ? No worries , here it is :

## Form Code 

~~~html

   <form id="contactform" action="#" name="contactform" netlify>
<section class="bg-red">
  <h2>Dear Kapil,</h2>
  <p>My
    <label for="name">name</label> is
    <input type="text" name="name" id="name" minlength="3" required></p>
</section>
  <p>My
    <label for="email">email address</label> is
    <input type="email" name="email" id="email" required>
  </p><br />
  <p>My
    <label for="number">mobile number</label> is
    <input type="tel" name="number" id="number" minlength="9" maxlength="14" required>
  </p><br />
  <p> I have a
    <label for="your-message">message</label> for you,</p>
  <p>
    <textarea name="your-message" id="your-message" rows="4" maxlength="10000" class="expanding" required></textarea>
    </p>
    <button type="submit">
      <svg version="1.1" class="send-icn" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="100px" height="36px" viewBox="0 0 100 36" enable-background="new 0 0 100 36" xml:space="preserve">
        <path d="M100,0L100,0 M23.8,7.1L100,0L40.9,36l-4.7-7.5L22,34.8l-4-11L0,30.5L16.4,8.7l5.4,15L23,7L23.8,7.1z M16.8,20.4l-1.5-4.3
	l-5.1,6.7L16.8,20.4z M34.4,25.4l-8.1-13.1L25,29.6L34.4,25.4z M35.2,13.2l8.1,13.1L70,9.9L35.2,13.2z" />
      </svg>
      <small><span style="color:#15B6B1">Launch</span></small>
    </button>
   </form>

~~~

## This Form Uses :

1.[Github Repository](#github-repository)

2.[Netlify](#netlify)

3.[MrHyde](#mrhyde)

4.[Erlen's Codepen](#erlens-codepen)

5.[Tufte CSS](#tufte-css)

6.[Custom CSS](#custom-css)

### Github Repository

I'm using Github Repository for source code of this contact form.

[github.com/sirkapil/contact](//github.com/sirkapil/contact)

This is link to Github Repository , you can clone it or fork it ! Any suitable changes through pull requests are welcome.

### Netlify

I'm using netlify to host my form , it deploy instanly any commit made to github repository. the data you submit in contact form is saved to my netlify account and they inform me about any form submission through mail along with a copy of your message.

>"As Github Pages serves static sites and has limited features so you don't have inbuilt contact form option there. Therefore, you have to rely on third party for contact form submission , but most of them sell/exchange private information of users submitted through contact form , even  google form uses private information for advertising. that's why , Netlify was my choice to store contact form data."
{:.message}

### MrHyde 

It is android app that I use to make suitable changes (commit) to my github repository. It lets me clone my github repository in internal storage of my phone and i can easily play with codes even without internet. I can push back changes to my github repository whenever connected to internet. and those changes are live instantly (few sec.)

### Erlen's Codepen

Major of source code is taken from  [Erlen's Codepen](https://www.erlen.co.uk/minimal-contact-form-with-expanding-textareas/).
I have made most of changes in  _contact.js_ , _contact.css_ and a few changes in _index.html_ file. Mostly changes are to make it compatible with _tufte css._

### Tufte CSS

Tufte CSS is inspired from Edward Tufte’s books and handouts. It was created by Dave Liepmann. This is github repository of _tufte css_
[github.com/edwardtufte/tufte-css](//github.com/edwardtufte/tufte-css)

>"I like _tufte css_ and implemented it in many blog posts. The best thing of tufte css is it's compatibility with side notes and marginal notes. Typography is really cool and looks amazing with any mathematical equation. it's background is clean and eye friendly , moreover looks like content is written on any sheet of paper. Another thing that i love about _tufte css_ is that it is printer friendly and looks great in pdf or printed format."
{:.message}

### Custom CSS

you will be thinking that how background color of contact form is changed from red to white. i've modified a part of _tufte css_ to change its background color to light red . it is using _custom css_ via `section` attribute and `class` tag as defined in starting of _custom css_.

~~~html

<section class="bg-red">

~~~

#### Code
{:.no_toc}

I'm giving you code of _custom css_.  you can change the background color via hsla or hex format. use any color picker tool and modify the _custom css_ for any colourful background.

~~~css

.bg-red {
  box-shadow: 0 0 200px 100px hsla(9, 100%, 95%, 1);
  background-color: hsla(9, 100%, 95%, 1);
}
/*Links: replicate underline that clears descenders */
.bg-red a:link { text-decoration: none;
         background: -webkit-linear-gradient(hsla(9, 100%, 95%, 1), hsla(9, 100%, 95%, 1)), -webkit-linear-gradient(hsla(9, 100%, 95%, 1), hsla(9, 100%, 95%, 1)), -webkit-linear-gradient(#333, #333);
         background: linear-gradient(hsla(9, 100%, 95%, 1), hsla(9, 100%, 95%, 1)), linear-gradient(hsla(9, 100%, 95%, 1), hsla(9, 100%, 95%, 1)), linear-gradient(#333, #333);
         -webkit-background-size: 0.05em 1px, 0.05em 1px, 1px 1px;
         -moz-background-size: 0.05em 1px, 0.05em 1px, 1px 1px;
         background-size: 0.05em 1px, 0.05em 1px, 1px 1px;
         background-repeat: no-repeat, no-repeat, repeat-x;
         text-shadow: 0.03em 0 hsla(9, 100%, 95%, 1), -0.03em 0 hsla(9, 100%, 95%, 1), 0 0.03em hsla(9, 100%, 95%, 1), 0 -0.03em hsla(9, 100%, 95%, 1), 0.06em 0 hsla(9, 100%, 95%, 1), -0.06em 0 hsla(9, 100%, 95%, 1), 0.09em 0 hsla(9, 100%, 95%, 1), -0.09em 0 hsla(9, 100%, 95%, 1), 0.12em 0 hsla(9, 100%, 95%, 1), -0.12em 0 hsla(9, 100%, 95%, 1), 0.15em 0 hsla(9, 100%, 95%, 1), -0.15em 0 hsla(9, 100%, 95%, 1);
         background-position: 0% 93%, 100% 93%, 0% 93%; }

.rounded-corners {
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  
}

body {
  background-color: hsla(60, 100%, 97%, 1);
}

#shortcut {
  position: fixed;
  top: 0.0em;
  left: calc( -112.391px + 1.5em );
  transform: rotate( -90deg );
  transform-origin: bottom right;
  /* background-color: hsla(60, 100%, 97%, 1); /*/
}

~~~

## Final Words 

Whatever i've used in this contact form is freely available on internet for personal use. However , it is my _dharma_ to give credit to such amazing persons without whom it couldn't be possible.

You can also use any of above feature and modify accordingly.
