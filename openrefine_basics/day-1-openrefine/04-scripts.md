---
title: "Scripts from OpenRefine"
teaching: 10
exercises: 5
questions:
- "Code generation from OpenRefine"
objectives:
- "Describe how OpenRefine generates JSON code."
- "Demonstrate ability to export JSON code from OpenRefine."
- "Save JSON code from an analysis."
- "Apply saved JSON code to an analysis."
keypoints:
- "All changes are being tracked in OpenRefine, and this information can be used for scripts for future analyses or reproducing an analysis."
---

# Lesson

## Scripts

* OpenRefine saves every change, every edit you make to the dataset in a file you can save on your machine.
* If you had 20 files to clean, and they all had the same type of errors, and all files had the same columns, you could save the script, open a new file to clean, paste in the script and run it. Voila, clean data.


>  - In the Undo / Redo section, click Extract, save the bits desired using the check boxes. 
>  - Copy the code and paste it into a text editor. Save it as a .txt file. 


To run these steps on a new dataset, import the new dataset into OpenRefine, open the Extract / Apply section, paste in the .txt file, click Apply.

