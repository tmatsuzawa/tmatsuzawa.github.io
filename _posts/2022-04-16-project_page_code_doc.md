---
layout: post
section-type: post
title: How to host a project documentation page on GitHub
category: professional, coding, documentation
tags: [ 'internal' , 'coding']
---
<h5> Task: Make a documentation website for a project</h5>
Okay. You have a project. You want to make a webpage and a documentation. Here is one way to do it.

For the webpage, you can use the [GitHub Pages](https://pages.github.com/) service.
For creating the documentation, you can use [SphinX](https://www.sphinx-doc.org/en/master/) which autogenerates a documentation from the docstrings.

<h5> Result </h5>

Check the [documentation page](https://tmatsuzawa.github.io/tflow/build/html/index.html) for my ```tflow``` project.

<hr>

<h3> Making a simple website with Github Pages </h3>
Github pages provides a simple way to make a website using Markdown.

With a pre-existing repository, 
1. On Terminal, ```cd``` to your repository.
2. Create a branch in your repo for your GitHub Page: ```git checkout -b gh-pages```
3. Create a markdown file called ```index.md```.
4. Push it to GitHub by using ```git push origin gh-pages```
<br>
Tips: Making a website may take a few minutes to complete. Make sure to clear cache when you renew the webpage.

It is not a bad idea to separate a repo about the project webpage and the documentation. 

References: 

- [Making a simple website with Markdown](https://kbroman.org/simple_site) <br>
- [Project Documentation with GitHub Pages](https://pennlinc.github.io/docs/Contributing/project-documentation/#project-documentation-with-github-pages)

<hr>
<h5> Making a code documentation webpage using SphinX</h5>
To do this, you need to install [SphinX](https://www.sphinx-doc.org/en/master/).


1. Install SphinX: ``` pip install sphinx```
2. ```cd your_project_directory```
3. ```sphinx-quickstart docs```... This makes a directory called ```docs``` and files like a ```conf.py```.
4. If you are using numpy or Google style docstrings, you must enable ```napoleon``` in the Sphinx ```conf.py```:
<br>... You can specify the SphinX theme in ```conf.py``` like ```html_theme = "sphinx_book_theme"```
<br>... For my project, I decided to use a third-party theme ```sphinx_book_theme``` which you can install using ```pip install sphinx-book-theme```.  
See [Sphinx Book Theme](https://github.com/executablebooks/sphinx-book-theme) for more details.

```
   # conf.py
   
   # Add napoleon to the extensions list
   extensions = ['sphinx.ext.napoleon']
   # Specify the theme
   html_theme = "sphinx_book_theme"
```
5. Build your API documentation:  ```sphinx-apidoc -f -o docs/source your_project_directory```
<br>... -f: overwrite existing files, -o: output directory
6. Edit your ```index.rst``` file
<br>... This will be the main page of your documentation.
<br>... The format is reStructuredText. [Quick reference](https://docutils.sourceforge.io/docs/user/rst/quickref.html#external-hyperlink-targets)
7. Generate html files: ```make html```
<br> This should create a directory called ```doctrees``` and ```build```.
8. GitHub recognizes your_project_directory/index.md as a default project website. Change this.
... Go to your repo webpage on GitHub, go to "Settings"->"Pages", and set source to "gh-pages/docs"
... GitHub Pages uses Jekyll as a default tool to make a website. You must disable it by creating an empty file called ```your_project_directory/docs/.nojekyll``` 
9. Commit and push the changes.

When you update the documentation, repeat Steps 5-9 except Step 8.


References:

Step1-3: [Sphinx Quickstart](https://www.sphinx-doc.org/en/master/usage/quickstart.html)
Step4: [Sphinx Google Style](https://www.sphinx-doc.org/en/master/usage/extensions/napoleon.html)


