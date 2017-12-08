+++
author = "Caleb Faught"
categories = ["Javascript", "Vue", "Web Development"]
date = "2017-11-01"
description = "Getting started with the Vue.js framework"
featured = "vue.jpeg"
featuredalt = "Vue logo"
featuredpath = "date"
linktitle = ""
title = "Getting Started With Vue.js 2.0"
type = "post"
draft = true
+++

# Why Vue.js 2.0?

Vue is a nice, easy-to-learn framework for building web applications that I personally think is a great stepping stone from Vanilla JS into the world of front-end frameworks.  Vue 2.0 is the latest iteration and includes nice modern features like a virtual DOM implementation.  This just means that instead of the JS framework re-rendering the whole page on each little change, it just updates the specific DOM element that is changed, meaning much faster rendering times. If you're a beginner coming from Vanilla JS, then a front-end framework will help abstract away some of the repetitive tasks like attaching event listeners, filtering data, creating reusable components, and binding data.

## Getting Started

The easiest way to get started with Vue is to instantiate a Vue object using a CDN. Add `<script src="https://unpkg.com/vue"></script>` to the end of the body in your HTML file, and underneath that link to your main JS file.

<script async src="//jsfiddle.net/ooz4kn5j/3/embed/html,result/"></script>
