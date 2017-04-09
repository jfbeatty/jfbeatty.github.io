---
title: Converting PDF files for use with LiquidText
author: Joshua Beatty
date: 2017-04-08
---

I've begun to use an iPad to annotate pdf files. Many apps let you highlight text and write comments that can be extracted as a text file. Currently I'm using [LiquidText](http://liquidtext.net/), but there are many other options. 

On files created from Word documents this works great. But if I'm working with an older pdf -- say, one from JSTOR -- it's painful to use. The OCR layer doesn't line up exactly with the visible text layer, so that as you try to highlight the visible text the selection is actually set off somewhat, and individual words are highlighted instead of a straight passage. Here's an example from Shari J. Stenberg, ["Liberation Theology and Liberatory Pedagogies: Renewing the Dialogue"](http://www.jstor.org/stable/25472152) (2006):

![Jagged OCR in Stenberg article](/images/stenberg-jagged-highlights.jpg)

The Stenberg article was also large -- 6.1 MB for a 21-page piece. I'm getting near the 2 GB limit on my paid Zotero account, and would rather not upgrade to the next level until I really need to. So I decided to see if I could use Adobe Acrobat to reduce the size of the document, and to run a new OCR scan that would allow me to more easily highlight and otherwise mark passages.

The process was simpler than I thought it would be. I opened the file in Acrobat and went to Tools --> Optimize Scanned PDF --> Optimize Scanned Pages. I tested several different settings but found that the defaults worked best:

![Default settings for Optimize Scanned Pages](/images/default-settings-for-optimize-scanned-pages.jpg)

The process took 2-3 minutes on my 21-page, 6.1 MB file. The resulting file was one-twelfth the size: 480 KB. But was the OCR improved?

![Optimized OCR of Stenberg article](/images/stenberg-optimized-highlights.jpg)

Yes! It was much easier to highlight passages, and the highlights look much better on the page.

P.S. On another PDF that was 53 MB but didn't have the offset OCR problem, when I tried “Optimize Scanned Pages,” it returned an error because the pages were already rendered. But just using “Reduce File Size” with default options brought the file size down to 7 MB.