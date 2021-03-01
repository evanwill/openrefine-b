---
title: Refine Basics
nav: Demo
---

- create project
- explore
- transform
- export

Let's look at the basic functions of OpenRefine using typical digital collection metadata.
Download:

- [`potlatch-historical-collection.csv`]({{ '/assets/potlatch-historical-collection.csv' | relative_url }}){:target='_blank' rel='noopener'} (from [University of Idaho Library](https://www.lib.uidaho.edu/digital/){:target='_blank' rel='noopener'})

**Create Project:**

- "Get data from" options
- "Configure Parsing Options", *check character encoding* (UTF-8!) and options, then give your project a name (names are easier to work with if there are no spaces or dashes) and click Create project.
- Refine never over writes your original data, it creates a copy!
- Information is *not* sent over internet. The data is copied into your workspace directory in Refine's specialized format (find your workspace directory by looking for the link at the bottom of the "Open Project" page).
- **Sanity Check**, ensure you have the expected number of rows! Keep this number in mind as you work through the project.

## Columns

Unlike most spreadsheets which focus on rows, Refine is column-centric.
Most operations are accessed via the column menus.

Explore:

- Text filter
- Facet > Text facet
- Facet > Customized facets > Facet by blank

Edit: 

- Edit individual cells (hover on value)
- Edit facets. Fix:
    - Format Digital (The digital file format of the resource, use [Internet Media Type (IMT) term](http://www.iana.org/assignments/media-types/media-types.xhtml).)
    - Type (The nature or genre of the resource. The general genre of object, using the DCMI type vocabulary.)
    - Language (language used in the object, [ISO 639-3](https://en.wikipedia.org/wiki/ISO_639-3))
- Transform column
    - Edit cells > Common Transformations > Trim leading and trailing whitespace
    - Edit cells > Transform > use [GREL](https://github.com/OpenRefine/OpenRefine/wiki/General-Refine-Expression-Language){:target='_blank' rel='noopener'}
        - add text, `value + " something new"`
        - find & replace, `value.replace("old","new")`
        - get values from other cells, `cells['column_name'].value`
        - [GREL dates](https://github.com/OpenRefine/OpenRefine/wiki/GREL-Date-Functions){:target='_blank' rel='noopener'}, `value.toDate().toString('yyyy-MM-dd')`
- Create new columns
    - Edit column > Add column based on... `value.length()`
    - Edit column > Split into several columns... 
    - *Note:* combining columns can be tricky because combining blank cells results in an error. Thus facet by blank first and combine only non-empty cells with a transform like `value + " " + cells["col 2"].value`
- Work with multi-valued cells
    - Edit cells > Split multi-valued cells... 
    - Edit cells > Cluster and edit...
- All column
    - Edit rows > Remove all matching rows
    - Edit columns > Re-order / remove columns
     - Star, Flag

## Project basics

Export:

- *Keep in mind:* export is always a new copy of data, never alters original! Your Refine projects will be automatically saved in your working directory and can be accessed from "Open Project" tab.
- *Subset:* if your current project is subsetted using filters and facets, the export will be the subset only. 
- Many export formats!
- templating

Undo / Redo & Automate:

- Undo / Redo
- Undo / Redo > Extract, copy json to txt file (use text editor, not Word)
- Undo/Redo > Apply, paste in saved extract and click Perform Operations
