# ems_cv_template
## Sources

I pulled from a few different sources to create this! 

The Google Sheets integration and printing functions came from Nick Strayer’s [datadrivencv](http://nickstrayer.me/datadrivencv/)

I adapted a [template created by Steven V. Miller](http://svmiller.com/stevetemplates/) for the CV layout (specifically the Academic CV template), which I combined with LaTeX’s generic pdf template so I could insert a bibliography. 

## Installation

You should just be able to clone this repository (or download all of the files using GitHub’s download ZIP option)

I’m assuming you already have R installed! But there are some libraries you’ll need; I’ve included code to paste into your R console to install them below for convenience (it’s very probable that I missed some that I already had installed – if so, let me know and I’ll update the list!). I also might not be using all of these libraries anymore as I built this in a very hodgepodge way… 

```r
install.packages("rmarkdown")
install.packages("magrittr")
install.packages("tinytex")
install.packages("vitae")
install.packages("tibble")
install.packages("tufte")
install.packages("fontawesome")
```

If this doesn’t work, it’s possible that the following might help:

```r
install.packages(”rsvg”)

devtools::install_github("nstrayer/datadrivencv")
```

## Generating a CV

You can then open the file called “CV_2023.Rmd” and “knit” it (press the yarn icon at the top of your R window). This should generate a pdf of my CV.

## Customizing!

### The Header

The first way to customize this is to change the header. You’ll notice a bunch of my information at the top, in between the two “- - -” lines. You can play around with formatting things if you’d like, but at the very least, I suggest changing the author, job title, email, phone, and web (so it’s no longer my info!). You can also uncomment other things, like github and twitter, if you’d like to include these.

### The Content

All the data in the CV are pulled from a google sheet where I’ve added a bunch of things. My sheet can be found [here](https://docs.google.com/spreadsheets/d/1WgfzqcE2shTZ1QICDNYhCWhuOU8HAZfZwL3r89Ea0b0/edit#gid=917338460). Make a copy of this sheet, then create a shareable link with the setting “Any on the internet with the link can view”. (I think there’s also a way to just generate this from a local .csv file on the original site). 

Next, replace the link in CV_2023.rmd (at line )with your new link. It will be empty until you fill it with information, but you can use mine as a guide or play around with creating your own headings. 

### The Publications

I created a collection in Zotero with the papers I wanted to include in my bibliography (which is automatically inserted at the end of your cv). Right click on this collection to export it, and save it as a .bib file to replace “CV_Pubs.bib” in your directory. 

 

The template uses apa-cv reference format, which can be changed by specifying a different csl file in the header (and adding this file to your directory).
