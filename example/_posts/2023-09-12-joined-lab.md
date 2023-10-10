---
layout: post
title: Joined Wildlife Pathogens Lab
image: /assets/img/blog/WildlifePathogensGroupPhoto.jpg
accent_image: 
  background: url('/assets/img/blog/caleb-george.jpg') center/cover
  overlay: false
accent_color: '#ccc'
theme_color: '#ccc'
description: >
  Overview of my new chapter as part of the Wildlife Pathogens Lab.
invert_sidebar: false
---

# Joined Wildlife Pathogens Lab

Joined Wildlife Pathogens Lab

* toc
{:toc}


## Wildlife Pathogen Lab's Goal
Most elements now have rounded borders, making the design look more modern (dare I say "Stripe-ified") than ever before. 

The goal of Hydejack was always to provide a theme that looks "designed" combined the amenities of a typical Jekyll theme for coders.
This is an important step in maintaining this goal.

At the same time, I'm introducing nerdy elements like [breadcrumbs](#serp-breadcrumbs), that are almost ornamental in nature.
You wouldn't find these on other Stripe-like designs, but I think they are appealing to developer types like myself. 
Like most additions to Hydejack, they can be disabled via configuration. 


## Meet the Team
The colors on the sidebar can now be inverted to allow brighter sidebar images. This can be enabled per-page in the fort matter:

```yml
invert_sidebar: true
```


## My Goals as Part of the Team
Code blocks can now have headers:

~~~js
// file: 'hello-world.js'
console.log('Hello World!');
~~~

Headers are added by making the first line a comment of the form `(file|title): ['"].*['"]`, e.g.:

    ~~~js
    // file: 'hello-world.js'
    console.log('Hello World!');
    ~~~
    
Code blocks with and without headers now also come with a copy button. 
In the case of header-less code blocks, the button only shows on hover to prevent potential overlap.


## Our Lab Website
Resumes can now have download buttons:

![Download Buttons](/assets/img/blog/9.1.0-3.png){:.border.lead width="1776" height="258" loading="lazy"}

Resumes can now have download buttons.
{:.figcaption}

The documentation has been updated with a chapter on [how to configure the buttons](/docs/basics/#downloads).




***
{:style="margin:2rem 0"}

There are many more changes and bugfixes in 9.1. See the [CHANGELOG](/CHANGELOG/){:.heading.flip-title} for details.



*[SERP]: Search Engine Results Page
