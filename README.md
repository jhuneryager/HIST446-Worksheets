# HIST 446 The Past as Data
## Ball State University

This repository contains the worksheet assignments for HIST 446 at Ball State University.

---

## Getting Started

### 1. Install R and RStudio

You need both. R is the language; RStudio is the program you'll use to edit your code scripts, visualize data, track variables, etc.

- [Download R](https://cloud.r-project.org/)
- [Download RStudio Desktop](https://posit.co/download/rstudio-desktop/)

Install R first, then RStudio.

### 2. Clone this repository

In RStudio: **File → New Project → Version Control → Git**, and paste the repository URL.

If you haven't done so yet, go ahead and also download GitHub Desktop to your machine. This is not a necessity, but it will help you understand how Git and version control works to have it alongside your RStudio environment.

### 3. Install the packages

This project uses [`renv`](https://rstudio.github.io/renv/) to record the exact version of every package the worksheets need. This means the code will still run the same way next semester and across different machines.

When you first open the project, run this in the console:

```r
renv::restore()
```

This reads `renv.lock` and installs everything. It will take a while the first time, but you only have to do it once. Good moment for a short coffee break.

If `renv::restore()` reports that `renv` itself isn't installed, run `install.packages("renv")` first, then try again.

### 4. Check that it worked

```r
library(tidyverse)
library(DigitalMethodsData)
data(gayguides)
head(gayguides)
```

If you see a table of data, you're good to go!

---

## How to Work Through a Worksheet

Each worksheet is a Quarto document (`.qmd`). It mixes explanation, example code, and prompts for you to complete.

1. **Open the `.qmd` file**.
2. **Run code chunks as you go** with the green arrow, or Cmd/Ctrl + Shift + Enter.
3. **Fill in the empty chunks and blockquotes.** Prompts are numbered and marked `(@)`. Blockquotes (lines starting with `>`) are where written answers go.
4. **Render the document** (click on the Render button) to check it works start to finish. If rendering fails, something in your code is broken. Keep calm, that's useful information and always fixable.
5. **Commit as you go.** Several small commits is the best way to keep your work progress safe, controlled and traceable. Remember: this is about reproducibility and transparency, and your commit history is part of what I'm looking at for your grade in the course.
6. **Push to GitHub** and submit the repository link on Canvas to complete a Worksheet assignment.
7. **Update your learning log** in `logs/`.

### A note on getting stuck

You will get stuck at some points when completing a Worksheet, and that is a-okay. What matters is what you do next: read the error, read the documentation, search for the message, ask for help. Record that process in your log. Remember that your grade will not be based on accuracy, but on your effort to find solutions and your demonstrated ability to troubleshoot when things don't work.

---

## The Worksheets

| # | Worksheet | What it covers |
|---|-----------|----------------|
| 1 | R Basics | Values, variables, vectors, functions, packages, data frames |
| 2 | Data Structures | Subsetting, matrices, the pipe |
| 3 | Loops, Conditionals and Functions | Control flow and writing your own functions |
| 4 | Basic Data Manipulation | dplyr verbs, `stringr`, regular expressions, missing data, factors |
| 5 | Advanced Data Manipulation | Grouping, joins, pivots, `forcats`, `lubridate` |
| 6 | Data Visualization | ggplot2, themes, color, export, visualization as argument |
| 7 | Exploratory Data Analysis | A workflow for approaching an unfamiliar dataset |
| 8 | Text Analysis | Corpora, tokenization, stopwords, tf-idf, co-occurrence |
| 9 | Topic Modeling | Document-term matrices, LDA, topics over time |
| 10 | Mapping | Geocoding, `sf`, choropleths, interactive maps with leaflet |

---

## Learning Logs

The `logs/` folder contains two templates. Copy the relevant one for each week and fill it in.

- `coding-log-weeks1-9.md` -- for the first half of the semester
- `coding-log-weeks10-finals.md` -- adds a section on documenting AI use

You may use AI tools in this course. What I'm asking is that you show your work: what you asked, what came back, what you kept, what you changed, and what you threw away. Critically evaluating an AI model's workflow suggestion is a valuable skill.

---

## Data

Most worksheets use the `DigitalMethodsData` package, which `renv::restore()` installs for you. A few download text corpora from a separate repository; those chunks are marked and the downloaded files are gitignored, so don't worry if they appear in your working directory.

---

## Credits

These worksheets were originally written by [Amanda Regan](https://github.com/regan008) for History 8500/8510 at Clemson University, and are adapted here with her permission.
