This repository is a meant to be a guide to generate a table of content for the book GameProgrammingPatterns.

The repo does NOT contain the book itself, either compile it yourself through the authors repository and convert it to a pdf or buy the book from the authors website [below](#requirements)

I usually like to read on my e-ink tablet but after purchasing the book as pdf I noticed that it didn't contain a table of content, I therefore went on to see what it would take (if possible at all) to add it to an existing pdf..

I stumbled over k2pdfopt which seemed to be just the tool I was looking for. Unfortunately by default it does a bunch of unwanted behaviors that we are not interested.

## Here's what you'll need
### Requirements
+ The book as pdf: GameProgrammingPatterns
    - get it here --> http://gameprogrammingpatterns.com

+ k2pdfopt: available for both mac, windows and linux:
    - get it here --> http://willus.com/k2pdfopt/

# generate table of content
I've done the leg work for you, the repository contains the .txt toc file you'll need for k2pdfopt to generate the pdf with our toc.

*The guide will assume you know basic cli (command line interface) usages*

*The guide is written for mac os but it's easily applicable to windows and linux.*

## Get started
Fire up your terminal and type:
```
$ ./k2pdfopt
```
You'll be introduced to this interface:   
![image](https://user-images.githubusercontent.com/1045397/45590982-de676480-b945-11e8-9304-26f952cd3dec.png)

k2pdfopt can do a lot of things and DOES by default... so to make sure it doesn't ruin (scale, reflow or similar) the pdf, we'll use a series of commands.

```
type: "<the path to the path pdf>" or drag the pdf onto the application
press enter
type: "-mode copy" (to copy the pdf without modifying its content)
press enter
type: "-n" (for native mode, ie. let text be text)
press enter
type: "-toclist <path to the .txt file>" (the path to the gameprogrammingpatterns.txt found in this repo)
+ press enter
+ press enter again and the program will start generating the new file
```

When the application is finished, you'll find the generated pdf in the same directory as the original pdf
