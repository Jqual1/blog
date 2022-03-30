---
title: Jonathon Qualls
layout: splash
classes: landing
permalink: /_pages/home/
read_time: false
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/img/splash0.jpg
  actions:
  - label: "About Me"
    url: "/_pages/about/"
excerpt: "I'm a guy who loves Game Design"
intro: 
  - excerpt: 'Throughout the years I have made many different projects and participated in polishing up many projects as well. From my personal projects to my class projects to my work at Disco Tray Studios, I am constantly working on stuff.'
feature_row:
  - image_path: assets/img/personal/art/gamedev.png
    alt: "placeholder image 1"
    title: "Game Dev"
    excerpt: "From Personal Projects to CSCI 151/370 to Disco Tray Studios projects. Here are all things Game Dev related."
    url: "/_pages/gamedev"
    btn_label: "Games"
    btn_class: "btn--primary"
  - image_path: assets/img/personal/art/webdev.png
    alt: "placeholder image 2"
    title: "Web Dev"
    excerpt: "From Personal Projects to CSCI 340 to Disco Tray Studios projects. Here are all things Web Dev related."
    url: "/_pages/webdev"
    btn_label: "Websites"
    btn_class: "btn--primary"
  - image_path: assets/img/personal/art/appdev.png
    title: "App Dev"
    excerpt: "Currently I have only helped in creating the Good Vibes app via ideas and testing, but in Fall 2022 I will learn App Dev."
    # excerpt: "From Personal Projects to Disco Tray Studios projects. Here are all things App Dev related."
    # url: "/_pages/appdev"
    # btn_label: "Read More"
    # btn_class: "btn--primary"
feature_row2:
  - image_path: assets/img/personal/art/23-3-22-logo.png
    alt: "placeholder image 2"
    title: "Placeholder Image Left Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Left aligned with `type="left"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row3:
  - image_path: assets/img/personal/art/23-3-22-logo.png
    alt: "placeholder image 2"
    title: "Placeholder Image Right Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Right aligned with `type="right"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row4:
  - image_path: assets/img/strawberry.jpg
    alt: "placeholder image 2"
    title: "Placeholder Image Center Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Centered with `type="center"`'
    image_caption: "My Strawberry Patch"
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %}
