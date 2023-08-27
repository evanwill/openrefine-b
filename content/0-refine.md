---
title: What is OpenRefine?
nav: Refine
---

OpenRefine is a <span class="term">[free](https://www.gnu.org/philosophy/free-sw.en.html){:target='_blank' rel='noopener'}</span>, [open source](https://github.com/OpenRefine/OpenRefine){:target='_blank' rel='noopener'}, standalone Java application for <span class="term">exploring, cleaning, and transforming data</span>, that runs offline in a web browser. 

{% capture text %}
The original creator [David Huynh](http://web.archive.org/web/20141021040915/http://davidhuynh.net/spaces/nicar2011/tutorial.pdf){:target='_blank' rel='noopener'} said Refine is:

## "A power tool for working with messy data"

- more powerful than a spreadsheet
- more interactive and visual than scripting
- more provisional / exploratory / experimental / playful than a database
{% endcapture %}
{% include card.html text=text %}

{% include figure.html img="refine.jpg" alt="openrefine interface" %}

Although Refine works with tabular data similar to spreadsheet programs, the interface is unique, providing column-centric menus used to manipulate views and subset your data.
It is not useful for traditional data entry, but is an incredibly powerful and flexible tool for a variety of data wrangling tasks.

{% capture usecase %}
<span class="term">Explore</span> - navigate and evaluate quality with visualizations and filters that help dig deeply into the data so you can get to know it better...

<span class="term">Clean</span> - efficiently discover and fix inconsistency with faceting, clustering, cell transforms, GREL expressions...

<span class="term">Enrich</span> - extend and enhance data by combining files, merging projects, fetching URLs, reconciliation with online databases...

<span class="term">Transform</span> - easily change formats, subset, or reshape with split/join multi valued cells, split columns, transpose columns/rows...

<span class="term">Automate</span> - record and preserve your processing routine for transparency, then automate reuse by exporting operation history in JSON!
{% endcapture %}
{% include card.html text=usecase header="Use Cases" %}

