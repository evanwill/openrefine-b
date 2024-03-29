---
title: Refine Basics
nav: Demo
---

Let's look at the basic functions of OpenRefine using demo data.
Download a CSV:

- [potlatch_historical_collection.csv]({{ '/assets/potlatch_historical_collection.csv' | relative_url }}){:target='_blank' rel='noopener'} (typical digital collection metadata from [University of Idaho Library](https://www.lib.uidaho.edu/digital/){:target='_blank' rel='noopener'})
- [university_wiki_data.csv]({{ '/assets/university_wiki_data.csv' | relative_url }}){:target='_blank' rel='noopener'} (messy data about University endowments harvested from Wikipedia, from the [Enipedia OpenRefine Tutorial](https://web.archive.org/web/20190105063215/http://enipedia.tudelft.nl/wiki/OpenRefine_Tutorial){:target='_blank' rel='noopener'})
- [doaj_article_sample.csv]({{ '/assets/doaj_article_sample.csv' | relative_url }}){:target='_blank' rel='noopener'} (citations harvested from DOAJ, from [Library Carpentry OpenRefine](https://librarycarpentry.org/lc-open-refine/){:target='_blank' rel='noopener'})

----------

## Refine Home Page

On Refine's home page you will see three main options on the left side tab menu:

- <span class="term">Create Project</span> -- this is where you start a new project--we will cover everything in next section! 
- <span class="term">Open Project</span> -- all your projects will be saved in your "workspace directory" and can be reopened at any time on this computer. This menu allows you to manage, open, and delete your saved projects.
- <span class="term">Import Project</span> -- complete Refine projects (including history) can be exported as an archive file (".tar.gz") to share or preserve. This option allows you to open the archive to use the project. Importing will create a new copy of the project in your "workspace directory".

----------

## [Create Project](https://openrefine.org/docs/manual/starting)

This menu will take you through loading and parsing data to start a new Refine project:

- <span class="term">"Get data from"</span>
    - This first menu offers a variety of sources for loading data to start a new project--from pasting in a clipboard to connecting with a Google Sheet. The most commonly used is loading a file from your local machine.
    - *Choose options:* "This computer" > Browse (select file) > Next
    - At this point Refine says "uploading data"--it might be more accurate to say copying or loading data. Information is *not* sent over the internet and your original data is never over written. Refine copies the data into your "workspace directory" into its own optimized internal format.
- <span class="term">"Configure Parsing Options"</span>
    - Once you have loaded a data source, this screen provides detailed options for parsing the contents and a preview of the results.
    - "Parse data as" -- generally Refine guesses the correct type of data format, however you can manual select an option if necessary. Each type will have a variety of parsing options to control the import process, ensuring that your data does not become corrupted. As you select parsing options the preview window will update, giving you visual feedback on the process. Keep in mind that the preview only loads the first 100 rows, so issues deeper in your data may not be immediately apparent.
    - "Character encoding" -- click in the box to select the correct character encoding. This is especially important on Windows to avoid mangling UTF-8 files.
    - "Project name" -- give your project a name, preferably without spaces or special characters. It is helpful to follow a descriptive filenaming convention to keep organized and remember what you were doing with this particular instance of the data (e.g. adding a date or identifier).
    - Click "Create Project" to finish parsing.

----------

## Project interface elements

Once loading and parsing your data is complete, the window will reload in the main project interface.
Overview of the main interface areas:

- Top bar:
    - Project name (upper left) -- can be changed by clicking in the box. 
    - "Permalink" (near the name) -- copy this link (right click, copy link) to grab a reuseable link that can restore a view with the currently applied set of filters and facets. This link is only usable on your computer and this copy of the project.
    - "Open" (upper right) -- clicking this will open the Refine home page in a new tab.
    - "Export" (upper right) -- we will cover this in the Export section below!
    - "Help" (upper right) -- a link to the [Refine user manual](https://openrefine.org/docs).
- "Facet / Filter - Undo / Redo" pane (on left) - toggles between:
    - "Facet / Filter" displays the currently applied filters/facets.
    - "Undo / Redo" displays the full history of operations on the project.
- Table area:
    - Row count -- this is an essential piece of information! Use the row count as a **coherence check**--always ensure you have the expected number of rows after creating the project and running operations. Keep this number in mind as you work through the project.
    - "Show as: rows records" -- [rows vs records](https://openrefine.org/docs/manual/exploring/#rows-vs-records) is an important concept that can cause confusion. If you don't want Refine to parse the record groupings, ensure the first column of your data has NO blank values!
    - "Show: 5 10 25 50 100 500 1000 rows" -- the limited preview and pagination allows the Refine interface to remain quick and responsive, as well as minimizing distraction.
    - "first" "previous" "next" "last" -- pagination buttons allow you to step through the rows of your data. Jumping to "last" is often a good **coherence check** when importing your data since scrambled parsing tends to result in messed up rows at the end.
    - Column menus -- each column has a menu accessed by clicking the down arrow next to the name. This is where most Refine operations are accessed. The "All" column is added by Refine to provide some special functions.

----------

## [Explore](https://openrefine.org/docs/manual/exploring)

Refine provides a variety of features to explore and learn about your data, diving into the details to discover the contents.
Most of these operations are accessed via menus on each column and act on the values in that column.

Applying Text Filter, Facets, or Sort are means to fluidly subset your data, changing your view of it. 
These do not make any changes to data directly.
You can apply multiple filters and facets at the same time to build a more complex set of conditions for your subset.

- <span class="term">Text Filter</span>
    - invert, reset
- <span class="term">Facet</span> 
    - "Text facet"
        - include, invert, reset
        - sort by name / count
        - choices
    - "Customized facets" > "Facet by blank"
- <span class="term">Sort</span>
    - Sort will add "Sort" menu at the top of the table, near the "rows" options. This indicates the sort is applied to your view. However, it is only a *view*, the data has not been changed. 
    - To permanently change the order of the rows, click the sort menu and select "Reorder rows permanently"

----------

## [Transform](https://openrefine.org/docs/manual/transforming)

Once you get to know your data, it's time to start cleaning.
The features used to explore data become the means to isolate issues so that you can apply operations to fix groups of rows/cells with similar problems. 

- <span class="term">Edit cell</span> -- hover over individual cell to edit value.
- <span class="term">Edit facet</span> -- hover over facet to edit all cells with that value. This is a fast and powerful way to mass edit.
- <span class="term">Edit cells > Transform</span> 
    - "Common Transformations"
    - "Transform" -- use the [GREL](https://openrefine.org/docs/manual/grelfunctions){:target='_blank' rel='noopener'} mini-language to manipulate cell values. The transform window provides a live preview allowing you to debug your expressions.
        - add text, `value + " something new"`
        - find & replace, `value.replace("old","new")`
        - get values from other cells, `cells['column_name'].value`
        - [GREL dates](https://openrefine.org/docs/manual/grelfunctions/#date-functions){:target='_blank' rel='noopener'}, `value.toDate().toString('yyyy-MM-dd')`
- <span class="term">Edit column</span>
    - "Add column based on..." -- this option adds a new column to your project, using a GREL expression, which is a common strategy for cleaning your data in Refine. Creating a new column allows you to check against the original to ensure your transformation goes as expected.
        - `value.length()`
    - "Split into several columns..." -- this powerful option can split multi-valued fields into separate columns.  
    - "Add column by fetching URLs..." -- this allows you to retrieve information from the web, i.e. web scrape directly from your table. This is very useful to harvest information or hit APIs that can enrich your data. Once harvested GREL provides HTML, XML, and JSON parsing abilities to transform the results.
        - e.g. IIIF api recipe: `"https://digital.lib.uidaho.edu/digital/iiif/phs/" + value + "/info.json"`
- <span class="term">Multi-valued cells</span>
    - "Edit cells" > "Split multi-valued cells..." -- splitting multi-valued cells will result in more rows in your project, so take care with the [rows / records](https://openrefine.org/docs/manual/exploring/#rows-vs-records) distinction. Once you split in one column, you generally should not run transformations on any other columns until you put the split back together with "Join multi-valued cells". 
    - "Edit cells" > "Cluster and edit..." -- Refine provides several builtin clustering methods to help clean up values in your data. See [Clustering in Depth](https://github.com/OpenRefine/OpenRefine/wiki/Clustering-In-Depth) for details.
- <span class="term">All</span> column
    - Edit rows > Remove all matching rows -- a common transformation approach is to isolate a subset of rows to delete from the project.
    - Edit columns > Re-order / remove columns -- this menu allows rapid transformation of the order of all columns.
    - Star, Flag -- provides markers that can be used to develop new subsets for transformations.
- <span class="term">Undo / Redo</span>
    - *Be brave!* Undo / Redo tab records every operation applied to your data. You can always check your history and undo anything. This is a great feature for transparency to verify how your data was transformed before analysis.
    - *Note:* only applied operations are recorded. Playing around with facets and filters that change only the view temporarily are not recorded. When an transformation is applied to a faceted view, the subset is recorded as part of that operation.
    - "Extract" -- opens a JSON object recording your operations. To save your process, copy the JSON into a text file (not Word). 
    - "Apply" -- paste in a save Extract JSON, then click Perform Operations to apply the exact processing routine. This is a great way to automate (or semi-automate) your data wrangling on repeating projects. *Note:* the data must be structured with the exact same column names.

----------

## [Export](https://openrefine.org/docs/manual/exporting)

Once you have wrangled, cleaned, and enhanced your data it is time to export it for your next steps. 
Refine is great at transforming data from one format into another, so it's export options are particularly flexible and useful.

The export is always a new copy of the data, never altering or over writing the original. 
Your project and its history are always autosaved in your "working directory", and can be access from the "Open Project" tab.

- <span class="term">Export</span>
    - When clicking the Export button, you will be exporting the current subset of your data, i.e. what you can view with the current filters and facets applied. This is amazingly helpful for creating data subsets quickly in different formats!
    - "OpenRefine project archive to file" -- this export is the internal Refine format. Only use this if you want to move or share the Refine project itself to another computer.
    - Many exciting formats available! (unlike Excel, Refine correctly encodes and formats all export options ensuring you will have good data for the next steps of your project)
    - "Templating" -- allows you to export *any* type of plain text file by editing the template elements and using GREL expressions. Each row will iterate through your template and be exported to a plain text file. By default it is set up to export JSON, but can be modified to create anything--transform your table into a novel!
