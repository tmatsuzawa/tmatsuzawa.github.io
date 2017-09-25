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

<p> layout: post <br>
section-type: post <br>
title: How to make a blog post using Jekyll <br>
category: documentation <br>
tags: [ 'test' ] </p>


<h2> Inserting images and resources </h2>
<h3> How to insert an image:</h3>
<p> You may use a definite path on Github. </p>
<img src="https://tmatsuzawa.github.io/img/2017-09-23/Keep_Calm.jpg"  >
<p> Image Example: Keep Calm and Research On <\p>

<p> [Keep Calm. Research On!](https://tmatsuzawa.github.io/img/2017-09-23/Keep_Calm.jpg) </p>
<p> You can also use the variable "url" which is defined in _config.yml </p>
<p> [Keep Calm. Research On!]({{site.url}}/img/2017-09-23/Keep_Calm.jpg) </p>
[Keep Calm. Research On!]   <a href={site.url}/img/2017-09-23/Keep_Calm.jpg> </a>

<h3>  How to insert a hyperlink:</h3>
<p> You may insert hyperlinks for images, pdfs, url, etc. </p>
<p> Link example, PDF:  <a href="https://tmatsuzawa.github.io/cv/CV_TakumiMatsuzawa.pdf"> Download Sample PDF </a></p>

<p> Hyperlink example: <a href="https://github.com/tmatsuzawa"> Here</a></p>


<h1> Recall your memory about HTML... <\h1>
<h1> This is a Heading h1. </h1>
<h2> This is a Heading h2. </h2>
<p> This is a paragraph.</p>