---
layout: home
title: publishing
permalink: /publishing/
---

# Introduction

This repository provides MAVRL's guidelines and templates for the writing of academic journal articles.

# A little bit of sermonizing

Before we begin, I should outline my philosophy and attitude towards the writing process. An academic article is the primary means through which you communicate your scientific results and ideas. The key to great scientific writing is logic flow, not language (though having a good command of English helps).

The logic of your article will be debated extensively during the writing process. This is where many logic gaps are exposed, often requiring further work to address. It is also a process in which you should feel free to argue with your co-authors (including your advisor) on the interpretation and flow.

Finally, writing, like all other components of your PhD/postdoc training, is an opportunity for learning a highly useful professional skill. The best students/postdocs are the ones who demonstrate a growth mindset for continuous improvement. For example, someone lacking in a growth mindset will simply click "Accept all changes"; someone that wishes to do better next time will review each change carefully, and perhaps even take the initiative to further improve on the changes that the advisor/other co-authors have made.

It has been my experience that good writing is correlated with scientific ability. Anyone with motivation and clear thinking can become a reasonable scientific writer. Anyone lacking either of those traits is not going to be a good scientist, no matter how good his language skills are.

# Preliminaries

These steps should be taken before any writing occurs:

* Discuss target journal(s) with your co-authors (especially your advisor). Journal impact factor (IF) should be a distant secondary consideration to appropriateness of journal. Excellent research published in an appropriate, reasonable IF journal will be read and cited more than in an inappropriate, high IF journal.
* Agree on an author list, especially who will be the first author(s) and corresponding author(s). Though this list may change as writing (and further research) progresses, early discussions help avoid disputes down the road.
* All co-authors are expected to contribute to the organization and drafting of an article. If your name appears anywhere on the author list, you should make sure this is an article that you will be proud to be associated with. Your responsibilities include both high-level input on content, interpretation of results, as well as more mundane things like proof-reading.
* All language settings should be standard English. Ensure this is the case if you are using Word. Indeed, English should be the setting for your office computer regardless of what your native language is. Any non-English font appearing on any document/presentation is unacceptable in our group. If you wish to default to another language, you are welcome to do so with your personal computers.
* Reading the literature as well as our group's papers are good ways of learning proper scientific writing style and article organization. It is what a professional would do.

# Collaborative articles

If our group is the lead for an article, the first author(s) will be responsible for coordinating all inputs from collaborators. This means not only getting the inputs in a timely fashion, but also editing those inputs into a consistent flow within the article. You should also feel free to request the inputs (e.g., text, references, figures, etc.) in the format that is desired by our group.

If we are providing input to an article led by another group, you should follow the guidelines set by the lead author. All inputs should also conform to the same professional standards as all other articles in our group.

# Software

* LaTeX or Microsoft Word are the only acceptable choices for word processors. In general, LaTeX (via [Overleaf](http://www.overleaf.com) is preferred unless the target journal explicitly indicates Word is preferred. When in doubt, discuss with your advisor.
* All references must be managed via Zotero together with the [Better Bibtex plugin](https://retorque.re/zotero-better-bibtex/). A new shared **private** group should be created for each paper. All co-authors should have access to this shared collection/folder. This shared collection/folder should contain all literature (with PDFs) relevant to the paper. 

# Templates and General Instructions

1. Use journal-provided templates if available.
2. If none are provided by the journal, two default templates (one for [LaTeX](/mavrl_latex_template.zip) and one for [Word](/mavrl_word_template.docx)) have been provided. Do not use default templates provided by Word.
3. All section headers should be properly styled. In LaTeX, this involves the use of the \section, \subsection, etc. commands. In Word, this means formatting the section headers with the Heading 1, Heading 2, etc. styles.
4. All figure/table captions and references should be cross-referenced. In Latex, this means you use the \ref\{\} command for figures and \cite\{\}, \citet\{\} or \citenum\{\} for references. In Word, this means you use the Insert Cross Reference command in referencing your figures in the text and Mendeley -> Insert citation for references. Learn to use these properly so that you do not spend unnecessary time renumbering figures and references during writing.

# Figures

Plots and figures are typically the most important part of your article. Many readers will first look at them to get a quick sense of what your key results are. You need to spend a lot of time making sure the data is presented in a logical and legible manner.

* All plots must have large, legible fonts. For presentations, imagine you are in a huge ballroom in a conference where the famous 80-year-old Nobel Laureate who may be in your future hiring committee is sitting at least 50 m away from your projected presentation. If he cannot read the plot without difficulty, you have failed.
* Note that the default line widths, marker sizes and fonts in most graphics software are usually unacceptably small. Remember that in papers, the editor is going to scale your graphic into a \< 5cm x 5cm in a typical two-column journal. Font sizes typically need to be \> 20 and lines need to be at least \> 3 weight.
* All graphical data should be prepared in **vector formats** such as SVG, EPS and non-image PDFs so that they can be scaled to arbitrary sizes without loss of resolution. Formats such as JPG and PNG are discouraged unless they are prepared from a graphic source with very high resolution. E.g., VESTA structure images tend to look good as PNGs. Even if the journal states that it prefers a non-vector format like JPG or TIFF, use vector formats first and convert to a high-resolution non-vector format later.
* Figures should be prepared in professional software such as matplotlib or matlab or Origin. Excel figures are generally extremely poor. But they can be acceptable in certain instances if you spend the time to make them look right.
* Learn the basics of color matching. There are simply some colors that do not go together. [Colorbrewer](http://colorbrewer2.org/) is a good resource. Know the difference between color schemes for sequential vs diverging vs qualitative data, and choose schemes that works well for the kind of data you have.

# Process overview

Writing a journal article comprises the following steps:

1. Preparing an outline
2. Drafting
3. Finalizing

## Preparing an outline

An outline should be prepared prior to any writing. This outline should include:
* The target journal and format (Letter/Full-length/Communication). Copy and paste the journal's formatting guidelines as an Appendix to the outline.
* All section headers. Even if you are writing an article that does not require section headers (e.g. a short Letter or Communication), you should use "virtual" headers to organize the flow of your writing.
* Bullet points for each section, especially the Results and Discussion sections.
* All figures that will be included in the article. Though the figures do not have to be publication-quality at this point, they must already be in reasonably good form that the key takeaways are clear. In particular, detailed observations and insights for each figure should be written out in bulleted form.

The outline is the most important document in the whole writing process. Clearing a well-structured outline with your advisor saves significant effort in actual writing.

## Drafting

Proper scientific writing is expected. In addition, these are my guidelines on proper writing style for papers:
* Start by making sure spelling and grammar checking are enabled. If you are using Word, make sure the checks are on the fly. If you are using LaTeX, use an editor that does it for you (like ShareLatex). A draft that is riddled with preventable spelling and grammar errors shows that you did not care enough to make an effort.
* All statements about how you carried out the work should be in the past tense. Statements of truth, e.g., ```Figure X shows <this fundamental principle>```, are in present tense.
* Active, not passive, voice is preferred.
* Third person, not first person.
* Sentences should be concise and with purpose. Do not add filler statements. Many novice writers equate quantity with quality.
* I write and rewrite all my sentences at least three times to achieve the clarity of message that I want. If you are not doing so, the likelihood is that you are not thinking hard enough about what you want to say.
* Scientific writing is about *precision*. If a word is vague, it should be avoided or supplemented with a precise description. For example, ```Property X shows a relationship with feature Y``` is imprecise. What kind of relationship? Linear? Exponential? Inversely related? Instead, ```Property X shows a linear relationship with feature Y, with X = 0.5 Y + 0.1.``` is precise.
* Consistency helps the reader process your results. For example, use units that are in common use in the specific field/application as far as possible.
* Even extremely complex concepts can be written in a way that a reader can follow the general train of thought with little effort. Bad writing generally shows that the writer himself does not fully understand the concepts and is rambling his way through in the hope that no one notices his ignorance. You should know the specific topic better than anyone else, including your advisor.
* All drafts should be prepared with single column and at least a line spacing of 1. If you are using Latex, setting the document type to "preprint" usually does the trick.
* All figures, tables and other floats should be inserted inline with the text close to where they are mentioned in the text. Do not bother with sizing and positioning your images to wrap around text while you are writing. The publishers do that for you.

During the drafting process, I will make extensive use of tracked changes and comments (for LaTeX, this is done via ShareLatex's system). Note that it takes a lot more effort to use tracked changes than to just edit your article without them. I do it because I want you to learn from the changes that are being made.

An academic paper generally comprises the following sections:

* **Abstract**. Highlight the key results and accomplishments of this work. This needs to be self-contained, such that if the reader can immediately decide if the rest of your article is deserving of further attention.
* **Introduction**. Introduce the reader to the topic, why it is important, and how your work adds to the body of knowledge. This is where you establish credibility. If your introduction is not sufficient, readers think you do not know what you are talking about. If your introduction is too long, people lose interest before they get to your results. Strike a balance between relevant background and convincing the reader that you have something new to say about the topic.
* **Methods**. Methods should be concise but descriptive enough for people to know that you have done your work correctly, as well as to reproduce your results. Methodology that has already been covered in previous literature should refer to the relevant works for details. Do not overburden the reader with too many details.
* **Results**. Results is where you present data. You need to structure this section with a proper logical flow. Start by writing your subsection headers so that you have an idea of how you want to present your results to the reader. Then add the appropriate figures and tables that best show the data that you want. Then write the text to guide the reader in understanding your data.
* **Discussion**. This section is non-optional and you are not allowed to combine Results and Discussion. The Discussion section is where you really go into the implications of your findings. What does your results mean for the field? Have you provided some fundamental insight into a scientific process? A good Discussion section is the difference between a mediocre paper and an insightful article.
* **Conclusion**. A brief summary of your findings and the implications, i.e., a summary of your results and discussion.
* **End matter**. Acknowledge all funding sources and computing resources used. It is *imperative* that you get this correct. Most journals also require other items such as summary of the supplementary information, conflicts of interest statement, author contributions, etc. Make sure all these are handled properly.

## Finalization

In this last step, you proof-read the entire paper for spelling and grammatical errors, ensure that all figures, tables, captions, etc. conform to the target journal requirements. You also draft a Cover Letter for submission.

# Recommended readings

These are books/resources that are recommended for understanding our group's preferred writing style.

* George Orwell's Essay on "Politics and the English language". Google for it.
* William Strunk Jr.'s "The Elements of Style". You can find it on Amazon or the library. 
