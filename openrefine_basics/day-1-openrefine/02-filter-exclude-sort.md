---
title: "Filtering and Sorting with OpenRefine"
teaching: 10
exercises: 10
questions:
- "Filtering and sorting data"
objectives:
- "Filter to a subset of rows by text filter or include/exclude."
- "Sort table by a column."
- "Sort by multiple columns."
keypoints:
- "OpenRefine provides a way to sort and filter data without affecting the raw data."
---

# Lesson

## Filtering

There are many entries in admissions table. We can filter it to work on a subset of the data in the list for the next set of operations.

1. Select **For what commited** drop-down menu **> Text filter**. Note that a **For what commited** facet will appear on the left margin.
2. Type in **&** and press return. There are 86 matching rows of the original 4821 rows
(and are selected for the subsequent steps).
3. At the top, change the view to **Show** 50 **rows**. This way you will see the first 50 rows.

> ## Challenge
>
> What causes are selected by this procedure?
> How would you restrict this to one of the causes selected?
{: .challenge}

### Excluding entries

While we could type more letters of text, or click **case sensitive**, another way to filter is to **include** and/or **exclude** entries in a facet. If you still have your facet for **For what commited**, you can use it, or use drop-down menue **> Facet > Text facet** to create a new one. Only the names that agree with your **Text filter** will remain.

> ## Challenge
>
> Use **include / exclude** to exclude one of the causes. Below are some suggested steps.
>
> 1. In the facet (left margin), click on one of the causes, such as **Assault & Battery*. Notice that when you click on the value, or hover
> over it, there are entries to the right for *edit* and *include*. 
> 2. Click **include**. This will explicitly include this cause, and exclude others that are not expicitly included. Notice that the
> option now changes to **exclude**.
> 3. Click **include** and **exclude** on the other causes (**Homeless & Destitute**) and notice how the two entries appear and disappear
> from the table.
{: .challenge}

## Sort

You can sort the data by a column by using the drop-down menu in that column.
There you can sort by **text**, **numbers**, **dates** or **booleans** (logical expressions). You can specify what order to put **Blanks** and **Errors**.

If this is your first time sorting this table, then the drop-down menu for the selected column shows : **> Sort...**. Select the way to sort (such as **numbers**) 

> ## Challenge
>
> Sort by month. How can you ensure that months are in order?
{: .challenge}

If you try to resort a column that you have already used, the drop-down menu changes slightly, to **> Sort** without the *...*, to remind you that you have already used this column. It will give you additional options:

* **> Sort > Sort...**
* **> Sort > Reverse**
* **> Sort > Remove sort**

### Sorting by multiple columns.

You can sort by multiple columns by performing sort on additional columns. The sort will depend on the order in which you select columns to sort. To restart the sorting process with a particular column, check the **sort by this column alone** box in the sort pop-up menu.

> ## Challenge
>
> Try sorting by a **year** after you have sorted by **month**. What happens to ordering?
>
> Try sorting first by **year** and then by **month**. Be sure to check the **sort by this column alone** box when sorting by **year** to remove earlier sorts.
{: .challenge}

If you go back to one of the already sorted colunms and select **> Sort > Remove sort**, that column is removed from your multiple sort. If it is the only column sorted, then data reverts to its original order.

> ## Challenge
>
> Sort by **year**, **month** and **day** in some order. Be creative: try sorting as **numbers** or **text**, and in reverse order (**largest to smallest** or **z to a**).
>
> Use **> Sort > Remove sort** to remove the sort on the second of three columns. Notice how that changes the order.
{: .challenge}
