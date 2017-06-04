---
title: "Working with OpenRefine"
teaching: 15
exercises: 20
questions:
- "Getting started working with OpenRefine"
objectives:
- "Create a new OpenRefine project from a CSV file."
- "Recall what facets are and how they are used to sort and summarize data."
- "Recall what clustering is and how it is applied to group and edit typos."
- "Manipulate data using previous steps with undo/redo."
- "Employ drop-downs to split values from one column into multiple columns."
- "Employ drop-downs to remove white spaces from cells."
keypoints:
- "Faceting and clustering approaches can identify errors or outliers in data."
---

# Lesson

## Creating a Project


Start the program. (Double-click on the openrefine.exe file (or google-refine.exe if using an older version). Java services will start on your machine, and OpenRefine will open in your Firefox browser).

Launch OpenRefine (see [Getting Started with OpenRefine](00-getting-started.html)).

OpenRefine can import a variety of file types, including tab separated (`*.tsv`), comma separated (`*.csv`), Excel (`*.xls`, `*.xlsx`), JSON, XML, RDF as XML, Google Spreadsheets. See the [OpenRefine Importers page](https://github.com/OpenRefine/OpenRefine/wiki/Importers) for more information.

In this first step, we'll browse our computer to the sample data file for this lesson. 

If you haven't already, download the data to your computer: [https://raw.githubusercontent.com/crowesn/beyond-tei/master/datasets/hor_v005_addedValue_notCleaned.csv](https://raw.githubusercontent.com/crowesn/beyond-tei/master/datasets/hor_v005_addedValue_notCleaned.csv)
[https://ndownloader.figshare.com/files/7823341](https://ndownloader.figshare.com/files/7823341)

Once OpenRefine is launched in your browser, the left margin as options to **Create Project**, **Open Project**, or **Import Project**. Here we create a project, which just takes a couple steps:

1. click **Create Project** to bring you to "Get data from" "**This Computer**".
2. Click **Browse...** and select file `hor_v005_addedValue_notCleaned.csv`. Click **Open** in the browse window to finish selection 
3. Click **Next>>** under the browse button to upload data into OpenRefine.
4. OpenRefine gives you a preview - a chance to show you it understood the file. If, for example, your file was really tab-delimited, the preview might look strange, you would choose the correct separator in the box shown and click **Update Preview** (look in bottom panel). If this is the wrong file, click **<<Start Over** (look in upper left region).
5. If all looks well, click **Create Project>>** (look in upper right corner).

Note that at step 1, you could upload data in a standard form from a web address by using "Get data from" "**Web Addresses (URLs)**". However, this won't work for all URLs.

## Faceting

*Exploring data by applying multiple filters*

OpenRefine supports faceted browsing as a mechanism for

* seeing a big picture of your data, and
* filtering down to just the subset of rows that you want to change in bulk.

Typically, you create a facet on a particular column. The facet summarizes the cells in that column to give you a big picture on that column, and allows you to filter to some subset of rows for which their cells in that column satisfy some constraint. That's a bit abstract, so let's jump into some examples. 

[More on faceting](https://github.com/OpenRefine/OpenRefine/wiki/Faceting)

>  - Scroll over to the _For What_ column.
>  - Click the down arrow and choose > Facet > Text facet.
>  - In the left margin, you'll see a box containing every unique, distinct value in the _For What_ column 
and how many times that value occurs in the column.
>  - Try sorting this facet by name and by count. Do you notice any problems with the data? What are they?
>  - Hover the mouse over one of the names in the Facet list. You should see that you have an "edit" function available. 
> You could use this to fix an error immediately, and OpenRefine will ask if you want 
> to make the same correction to every value it finds like that one (or not). But OpenRefine offers 
> even better ways to find and fix these errors, which we'll use instead.




> ## Exercise
>
> Using faceting, find out how many years are represented in the ~date~~.  
>
> Is the column formatted as Number, Date, or Text? How does changing the format change the faceting display?
>
> Which years have the most and least observations?
{: .challenge}

## Cluster

In OpenRefine, clustering means "finding groups of different values that might be alternative representations of the same thing". For example, the two strings "New York" and "new york" are very likely to refer to the same concept and just have capitalization differences. Likewise, "Gödel" and "Godel" probably refer to the same person. Clustering is a very powerful tool for cleaning datasets which contain misspelled or mistyped entries. OpenRefine has several clustering algorithms built in. Experiment with them, and learn more about these algorithms and how they work. 

>  - In the _For What_ Text Facet we created in the step above, click the _Cluster_ button.
>  - In the resulting pop-up window, you can change the Method and the Keying Function. Try different combinations to 
> see what different mergers of values are suggested.
>  - Select the _key collision_ method and _metaphone3_ keying function. It should identify three clusters. 
> Click the _Merge?_ box beside each, then click _Merge Selected and Recluster_ to 
> apply the corrections to the dataset.
> - Try selecting different Methods and Keying Functions again, to see what new mergers are suggested. You may find there are 
> still improvements that can be made, but don't Merge again; just Close when you're done.  We'll now 
> see other operations that will help us detect and correct the remaining problems, 
> and that have more general uses besides.


[More on clustering](https://github.com/OpenRefine/OpenRefine/wiki/Clustering-In-Depth)

## Split

If data in a column needs to be split into multiple columns, and the parts are separated by a common separator (say a comma, or a space), you can use that separator to divide up the bits into their own columns.


>  - Let us suppose we want to split the _Disposal_ column into separate colums for repeated outcomes. 
>  - Go to the drop-down tab at the top of the _Disposal_ column. Choose Edit Column > Split into several columns.
>  - In the pop-up, in the Separator box, replace the comma with a forward slash (/).
>  - Remove the check in the box that says "Remove the column".
>  - Click "OK". You'll get some new columns called _disoposal 1_, _disposal 2_, and so on.
>  - Notice that in some cases _disposal 1_ and _disposal 2_ are empty. Why is this? What do you think we 
should do about it?

## Undo / Redo

It's common while exploring and cleaning a dataset to discover after you've made a change that you really should have done something else first. OpenRefine provides Undo and Redo operations to make this easy.


>  - Click where it says Undo / Redo on the left side of the screen. All the changes you have made so far are listed here.
>  - Click on the step that you want to go back to, in this case the previous step. The added columns will disappear.
>  - Notice that you can still click on the last step and make the columns reappear, and back, and forth. 

## Trim Leading and Trailing Whitespace

Strings with spaces at the beginning or end are particularly hard for we humans to tell from strings without, but the blank characters will make a difference to the computer. We usually want to remove these. OpenRefine provides a tool to remove blank characters from the beginning and end of any entries that have them.


>  - In the header for the column _disposal_, choose Edit cells > Common transforms > Trim leading and trailing whitespace.


