# List of items covered here:

* What R Markdown is
* How to use R Markdown in RStudio to create .Rmd files
* Structure of these files and how to use them to make reports
* what code chunks are and how to include them in the documentation
* How to take all the analysis done and transform it form an .Rmd file into a report


# Documentation-with-R-Markdown

* A file format for making dynamic documents with R.
* R Markdown lets us create a record for our analysis and conclusions in a document.
* It helps tie the code and the reports so we can share every step of our analysis.

# R Markdown 

* It is a syntax for formatting plain text files.
* It helps us convert the file into lots of different formats like HTML, PDF, Word Documents, or convert to a dashboard or slide presentation.

# R Notebook 

Lets us run the code and show the graphs and charts that visualize the code.

# Lets get strated with R Markdown

* Step 1: Open - File
* Step 2: Select - RMarkdown
* Step 3: Name the file and click "OK"
* Step 4: Click on file and "Save"

Now, you’ll transfer the code from the file you opened to a new R Markdown file so that you can write your own explanation of the steps you took. By doing this, you can create a more complete record of your overall thought process so that others will be able to understand it.

1. Open a new R Markdown (Rmd) file to begin building the basic structure of your notebook. Select File -> New File -> R Markdown.
2. In the dialog box that opens, add a title for your notebook. Name it something that will help you easily recognize what your analysis is about (e.g., “Penguins Plots”). 

3. Type your name in the Author field. 

4. For now, leave the file in the recommended html output format. When you render the file later, it will appear as an html report. You can always change it to a pdf or Word file later. 

5. Click OK. An R Markdown file will appear in a new tab in the script viewer pane. You should now have two tabs: one for the new Rmd file and one for your analysis. You can toggle back and forth between them when you need to by clicking on the tab you want to access.
6. Format your notebook

The first part of your notebook is the YAML header section. YAML is a language used in data files to improve human readability, and the YAML header section exists to provide information about a document to the humans reading it. RStudio automatically populates this section with the information you provide and other general information, such as the date you create the file.
Screenshot of th YAML header section with the title, author, date, and output format details

You can change the information in this section at any time by adding text or by typing over the current text. Notice that each line has a number associated with it. That makes it easy to reference a location in the notebook and also for you to track where you make changes in the notebook.

Again, RStudio automatically populates the notebook with this formatted default code chunk. This chunk basically means that your code will be shown in your final report when you’re ready to render it.

All code chunks begin and end with delimiters. To start a code chunk, you can type three tick marks followed by a lowercase “r” in curly brackets: ```{r} 

To end it, type just the three tick marks: ```

There are two shortcuts to adding code. On your keyboard, you can press Ctrl + Alt + I (PC) or Cmd + Option + I (Mac). Or you can click the Add Chunk command in the editor toolbar:
Screenshot of the RStudio Editor toolbar with the Add Chunk button selected

To add a code chunk to your Rmd file, follow these steps: 

1. Click the end of the last line of your Rmd file. Use either of the previously-mentioned shortcuts to create a code chunk.

2. Press Enter (Windows) or Return (Mac) two or three times after the default code chunk to create space between the existing code chunk and the next code chunk you will add. 

3. Copy the code from the analysis file you opened earlier and paste it in the gray area between the beginning and ending delimiters. 

4. Select the rest of the template content in the file and delete it. This gives you a blank space to work in to help avoid potential errors from mixing your own comments and code with the pre-existing ones in the template.

The white background is where you will type plain text with markdown syntax. As you learned earlier in this course, markdown is a syntax for formatting plain text files. Using markdown makes it easier to write and format text in your notebook. 

# Here are some basic formatting options:

* To start a new paragraph, end a line with two spaces
* To apply italics to a word or phrase, place an asterisk at the beginning and at the end of the word or phrase, for example, *italics works*
* To apply bold to a word or phrase, place two asterisks at the beginning and at the end of the word or phrase, for example, **bold is useful**
* To create a header, type a hashtag (#) followed by a space and your text for example: # Getting Started with R Markdown

When creating headers keep the following in mind:

* Headers will appear in blue
* A single hashtag is the largest header
* The more hashtags you add (up to six), the smaller the header

# To format comments in your notebook, follow these steps:

1. Click in a line above the code chunk you added but below the YAML section.

2. Type a main header for your report using a single hashtag. You might want to restate the title in the YAML in a different way or add to it with a short description.

3. Add a smaller header below that to label the first part of your programming. Follow that with a description of the code chunk that you added.
Screenshot of a formatted R Markdown text file

Tick marks format the text to appear as code even though the text is not in a code chunk. The tick marks in the code above create a gray background behind “tidyverse” and “palmerpenguins.”
Continue formatting

Keep working on your formatting until you have at least three levels of headers and more descriptions for your analysis. At any point, you can click Knit in the script pane to render the file.

When you render your file, you can preview how it will look in the format you selected when you opened the file. In this example, you will preview an html file.
Screenshot of a formatted R Markdown html file

Rendering a file also automatically runs the code chunks to show the output. In this example, it shows that tidyverse was loaded using the library() function.

# YAML

A language for datathat translate it so it's readable. It originally stood up for: Yte Another Markup Language.

* In RMD file, first section is of metadata: "Title, Author, Date, Output" between "---" and endign with same "---"
* The test ion the RMD file is inserted between "---{r}" and "---"
* A hashtag(#) will create a header section, the more the hashtag, the smaller then header.
* An astreak(*) will italicise the word.
* The double astreaks(**) will bold the word.
* To insert a url "<https://......>"

To add bullets:

* Add an astreak(*).

To embedd the link to avoid the clutter when its too long:
* Click here to visit the [link](http://rmarkdown.rstudio.com).

Embedd the image:
* ![Plot this way](http://pikaby.image.com).

# Code Chunk

Code added in an .Rmd file.

# Delimeter

A character that indicates the beginning or end of a data item. i.e: ```{r} and ```.

Code chunk keyboard shortcuts.

* Macbook: Command+option+I

* PC/Chromebook: ctrl+alt+I
* RStudio: Code + Insert_chunk

## Example of an .Rmd file:

---
title: "ggplot_hook"
author: "Dhwani"
date: "2024-02-23"
output: html_document
---

## Setting up my environment

Notes setting up my R environment by loading the 'tidyverse' and 'plamer penguins' packages.

```{r packages}

library(tidyverse)
install.packages("palmerpenguins")
library(palmerpenguins)
```

# Exporting Documents:

Any .Rmd file once finished, can be converted into .html, .pdf or word format. Just click on the down arrow next to the 'knit button'



# Additional resources

* https://colab.research.google.com/notebooks/intro.ipynb
* https://www.kaggle.com/docs/notebooks
* https://gtribello.github.io/mathNET/assets/notebook-writing.html




