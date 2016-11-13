---
title: My workflow for academic writing on Mac and iPad
author: Joshua Beatty
date: 2016-11-06
---

When I recently purchased a new computer I thought I'd take the time to set it up properly. I wanted to set it up to create an efficient workflow for academic writing, and one that would allow me to choose either a text editor or a more writing-focused program like Scrivener or Ulysses according to the needs of a particular project. I wanted to be able to integrate Zotero into the workflow, and I wanted to be able to write on my iPad and to be able to add citations from there as well.

My solution draws heavily on two sources: Dave Smith's ["Academic Writing with Scrivener, Zotero, Pandoc and Marked 2"][smith], and Dennis Tenen and Grant Wythoff's ["Sustainable Authorship in Plain Text using Pandoc and Markdown"][sustainable]. But it has some differences from both. For one, while Smith likes to write on a rich-text editor that's set to look like a plain-text editor, I prefer to write in an environment with serifed, differently-spaced fonts, even if I'm writing in a plain-text editor. (This only applies to prose writing, not coding). I also find that BibTeX does not work well for the particular sources I cite. As a historian, I often cite primary sources -- letters and manuscripts -- and Zotero's own CSL processor handles those much better than does BibTeX. 

Components:

- Zotero - bibliographic management
- Better BibTeX - Zotero plugin that exports your library to machine-readable forms like BibTeX, JSON, or YAML, and adds a citation key.
- Sublime Text - text editor
- Pandoc Academic - package for Sublime Text that adds syntax highlighting for Pandoc-flavored Markdown, including citations
- Scrivener - rich-text editor that can compile to many different formats, including MultiMarkdown
- zotpick-pandoc - script for easily accessing Zotero from programs other than Word or LibreOffice, generally referred to as Cite While You Write. Relies on Better BibTeX
- Marked 2 - convenient previewing of documents from either Sublime Text or Scrivener, using a Pandoc custom processor
- Pandoc - universal document converter

On iOS:

- Editorial: Ole Zorn's text editor. Can access files on Dropbox.
- BibTeX workflow for Editorial: allows access to a list of citekeys drawn from a YAML library
- Scrivener for iOS: mobile version of the desktop app
- Dropbox: stores the .md and .yaml documents necessary for this to work

## Sunday's work

Modified the syntax definitions in the Sublime Text Pandoc Academic package to account for unruly citation keys -- those with periods and hyphens in them. Could further refine this by using a regex that excludes spaces, commas, and left brackets rather than including a selected list of characters: 

~~~
@[^ ,\]]+
~~~

Having problems getting the Pandoc Academic's package to auto-produce output. Log says it can't find reference.docx. Tried to put that file into several different places, including joshua/.pandoc -- nothing worked.

[smith]: https://davepwsmith.github.io/academic-scrivener-howto/
[sustainable]: http://programminghistorian.org/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown