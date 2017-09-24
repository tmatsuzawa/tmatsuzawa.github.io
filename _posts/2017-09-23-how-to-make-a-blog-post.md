---
layout: post
section-type: post
title: How to make a blog post using Jekyll
category: documentation
tags: [ 'test' ]
---

<p> All information here is based on https://jekyllrb.com/docs/frontmatter/  </p>

<p> All blog post files must be stored under _post as markdown files (.md). The title of the post file must be YEAR-MONTH-DAY-title.MARKUP.
They must begin with YAML Front Matter, which looks like... </p>

<p> layout: post </p>
<p>section-type: post </p>
<p>title: How to make a blog post using Jekyll </p>
<p>category: documentation </p>
<p>tags: [ 'turbulence' ] </p>
</p>



<h1> This is a Heading h1. </h1>
<h2> This is a Heading h2. </h2>
<p> This is a paragraph.</p>

<h2> Inserting images and resources </h2>
<h3> How to insert an image:</h3>
<p> You may use a definite path on Github." </p>
<p> ![Keep Calm. Research On!](https://tmatsuzawa.github.io/img/2017-09-23/Keep_calm.jpg) </p>
<p> You may use a definite path on Github or use the variable "site.url" </p>
<p> ![Keep Calm. Research On!]({{site.url}}/img/2017-09-23/Keep_calm.jpg) </p>
<p> ![Keep Calm. Research On!]({site.url}/img/2017-09-23/Keep_calm.jpg) </p>

<h3>  How to insert a hyperlink:</h3>
<p> You may insert hyperlinks for images, pdfs, url, etc. </p>
<p> <a href="https://tmatsuzawa.github.io/cv/CV_TakumiMatsuzawa.pdf"> Download CV </a></p>
<p>  </p>
<p> <a href="{site.url}/cv/CV_TakumiMatsuzawa.pdf"> Download CV </a></p>
<p> You can also check out my <a href="https://github.com/tmatsuzawa"> Github</a></p>

