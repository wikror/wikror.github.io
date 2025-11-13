---
layout: post
title: "My writing setup"
category: blog
keywords: Visual Studio Code, Markdown, pandoc, Zotero, article writing, research, Latex, bibliography, bibliography manager, scientific paper, citation, reference list
date: 2023-02-08
---

Recently, after finishing writing a co-authored paper, it turned out that doing references is still absolutely terrifying for some of my colleagues, and I realized that the way I have set up my process is actually much less popular (at least in philosophy) than I realized - hence I thought that sharing what works for me might help some people working in Humanities figure out a process that works best for them. A lot of the things have grown over time, so probably could be simplified in some way, but I'm waiting for another procrastination period to tweak it some more.

In general the process looks like this: I'm writing papers and notes in Markdown using VSCode (previously Atom, before GitHub pulled the plug on the project) with some plugins as my go-to editor, handling citations through Zotero with some plugins, and use pandoc to export to more readable formats and generate citations and sometimes do final tweaks on Overleaf. I'll go through each step below. The notes should be sufficiently detailed as I intend to use this post also as a reference sheet for my future self!

## Reference database
[Zotero](https://www.zotero.org/) is probably not *that much* better from alternatives like Mendeley, for me the selling point was that it's free, open source, not Elsevier-owned and much more intuitive than Mendeley with which I played for a while and just couldn't make sense of.

Input of citations is a blast, you can import papers by their DOI, books by their ISBN, arxiv preprints with their IDs and it works hassle-free in like 90% of cases. If you need to add something manually it's also quite easy, and for book chapters I just add the book through ISBN and then change its type to Book Section and add missing data, like chapter title and authors.

I use one main add-on: [Better BibTex for Zotero](https://retorque.re/zotero-better-bibtex). This is to keep the citation keys meaningful to me and consistent over time (and different computers), as well as to set an automatic export into a bib file for further steps of the process.

Importantly, I have a single, very large, and a bit private file for references, hence whenever I have to upload it to the journal or elsewhere, I use [JabRef](https://docs.jabref.org/advanced/entryeditor/latex-citations) to filter only cited entries into a separate library which then gets submitted.


## First drafts
[Markdown](https://daringfireball.net/projects/markdown/syntax) is my go-to choice of a file format, as it is plain-text, future proof format, that makes me quite confident I will be able to access my notes and drafts in a few years time (provided I'll find them, as organizing files is not my strong suite...). I use the Visual Studio Code for writing, with several extensions: [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one), [Word Count](https://marketplace.visualstudio.com/items?itemName=ms-vscode.wordcount) and, crucially, [Pandoc Citer](https://marketplace.visualstudio.com/items?itemName=notZaki.pandocciter) for autocompletion of bibtex citation keys (remember to put path to the bibtex file in square brackets in extension settings!).

## Pandoc
Whenever I have to share a version of the paper, I'll process it in [Pandoc](https://pandoc.org/index.html) into a more accessible format, this is pretty straightforward and works out of the box.

## Google Docs
The setup so far works for single authored papers. For sharing with others I use mainly Google Docs, which has all necessary tools for collaborative writing (version history, tracking changes, comments). Overleaf might be a way to go here as well, but requires paid subscription for tracking changes.

## Overleaf
Given that journals' LaTeX templates tend to require a very specific setup of LaTeX environment and getting them to compile locally is a pain, I have given up on maintaining a local installation and opted for [Overleaf](https://www.overleaf.com/), which works perfectly well out of the box for most purposes. Then I will potentially download the final TeX file to process it with JabRef, as indicated [above](#reference-database).

## stackedit.io
For collaboration directly on a markdown file, I have been using the online editor stackedit.io, which allows connecting it to Google Drive, where the file is hosted, and has some basic conflict resolution implemented (though I worked in turns and did not test it thoroughly, so no guarantees). Probably Notion can be used as well for this purpose. Both have the 