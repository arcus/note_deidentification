## Creating an ontology

A coding ontology for a project like this balances several priorities, some of which conflict: 

- ease of use and understandability for human coders
- compatibility with the categories produced by NLP models
- ability to preserve as much non-identifying information as possible (reduce false positives), perhaps with special focus on particular kinds of information that are of most interest to a given research team
- comprehensiveness of resulting annotations, to provide a rich and detailed gold standard dataset for model assessment
- person-hours required to complete coding
- coverage of categories that meets or exceeds HIPAA requirements for de-identification

Of these, the last (adhering to HIPAA) is a hard requirement -- the balance for the others is a judgment call, and different projects may rank priorities differently. 

## Considerations for coder training


# Creating these documents

The coder training procedure document and annotation guidelines are markdown files intended for use with [LiaScript](https://liascript.github.io/). 
LiaScript is an open source markdown parser designed for educational content. 
If you want to learn more about how the Arcus Education team uses liascript, check out our [education module docs](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/docs.md#1), which includes details about metadata we include as well as things like [quiz questions](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/docs.md#quizzes-automatically-graded-questions) and [highlight boxes](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/docs.md#including-highlight-boxes).

Note that LiaScript won't work for private repos, or repos on Enterprise GH, which is why these documents are hosted on github.com.

Image files (including gifs) are stored in the media directory of this repository. 

There is metadata at the top of each LiaScript markdown file. 
The `version` field is particularly valuable, because it allows you to transparently reference previous versions. 
When you open a liascript file, it will default to the current version, but if you go to https://liascript.github.io/course/ you can select previous major versions as well. 

## Annotation guidelines

The goal for this document is for it to serve as a useful reference to coders as they annotate. 
The expectation is that a coder getting ready to work would pull up both their Arcus Lab and, in another tab, the annotation guidelines. 

The heading structure in the Ontology section (a heading for each category in the ontology) is intentional -- it results in one page for each category in the rendered liascript site. 
This makes navigating to a particular category easy via the table of contents on the left, and it also makes it possible to share a link to a specific category in the ontology (e.g. the [NAMES](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/note_deidentification/main/annotation_guidelines.md#names) category), which is useful for a group of coders communicating with each other. 

Brat allows entities that can be checked as well as categories selected from the ontology -- this effectively allows for a second dimension of information in the coding. 
In the current ontology, we created two of these [additional options](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/note_deidentification/main/annotation_guidelines.md#additional-options), "NonIdentifying" and "Unsure". 
Other ontologies have made use of that kind of tool to denote referent (such as "patient," "family member," and "hospital staff," so that a coder can label a span as, for example, "phone number" and then select "patient" to indicate it's a patient phone number).

## Coder training procedure

This document outlines the process for a new coder to learn to use this ontology. 
It includes both a training component and a reliability check. 
