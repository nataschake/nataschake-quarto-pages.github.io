# Building presentations from plain text using Quarto

## Intro

These are instructions how to create awesome "Ontotext"-themed *html* presentations using plaintext.

The process uses [Quarto](https://quarto.org/) to do the conversion from *markdown* to *html* and [reveal.js](https://github.com/hakimel/reveal.js) as a presentation framework.   

[Here](https://presentations.ontotext.com/gdb-connectors.html) is an example presentation, built form [this](https://gitlab.ontotext.com/trainings/training-demo/blob/master/7.Connectors/slides/Slides.md) source. 

## Steps to build a presentation 

### 0. Install Quarto 

**Don't** use the repos, install from Quarto's [download page](https://quarto.org/docs/get-started/).

### 1. Clone the project

`git clone git@gitlab.ontotext.com:sol/presentations.git`

### 2. Write your presentation 

The presentation is in [Quarto markdown](https://quarto.org/docs/authoring/markdown-basics.html), based on[pandoc markdown](https://pandoc.org/MANUAL.html#pandocs-markdown), which is very similar to the standard markdown everybody knows from gitlab and github. Here is a [markdown cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
The presentation syntax is really simple - section headings define the slides. Anything between is rendered in the slide. 

You can build  2d presentation with level 1 headings `# title of the part` define the columns and level 2 headings `## title of the slide` define the slides. 
For a linear presentation use only level 2 headings.

The [presentation.qmd](/markdown/sample/presentation.qmd) file in this projects runs over the most common slide configurations. You are encouraged to use it as a starting template for your own creations.  

Include the following *yaml* block (with starting and ending `---`) in the beginning of the *.qmd* file. This is information about the title slide and parameters for *reveal.js*. Use quotes if you include non alphanumerical characters. 


```yaml

---
author: "Your Name"
title: "The title of your presentation"
date: "01/01/1970"
format: revealjs
---
```

Only *title* and *format* attributes are required, *author*, *subtitle*, *date* are optional, but are very welcome. 
 
Several other parameters such as the theme, transition and syntax highlighting styles are also required by *reveal.js*. For convenience they are included in a separate yaml file [here](../_metadata.yml). However, you can tune the appearance of slides (custom background, custom transition options etc.) and store it into *markdown/your-folder/_metadata.yml*. It will have the priority over [common appearance](../_metatada.yml).

### 3. Compile html presentation

If you use the *presentation.qmd* file from this project you can use the following command in the command line:

`quarto render`

*_site_/markdown/your-folder/presentation.html* contains your presentation.

The list of all presentations is updated automatically.