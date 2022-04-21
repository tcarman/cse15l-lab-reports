# Lab Report 2

21st of April 2022

Contained here are a list of three bugs, the causes and the fixes to make a file pasring section of code work as intended.

## Bug One

![Bug One](LabReport2SS1.png)

The first bug explored here is a file without a link included at all. Before this change a file without a valid link would result in an infinte loop, only ending when manually kiiled or the program runs out of storage to use. The applied fix by passes the loop in the event that the file lacks a link in it. Passing the below file through would result in an infinate loop. 

[Bug One](https://tcarman.github.io/cse15l-lab-reports/blank.html)


## Bug Two

![Bug Two](LabReport2SS2.png)

This screenshot covers two different bugs. 

The first bug is a set of brackets,[], in one part of a the document and a set of paretheses,(), in another part of the document. Since this is not a valid link, this should not be included in a list of links. The solution for this is to add a clause, seen in the first if statement, designed to check to see if the brackets and paretheses are next to each other, thus making it a valid link. 

The second bug fixed in this image is treating an image as a link. Since with markdown, images and links have similar, but not idetical, syntax, the code can be easily confused to return the image as a link. The fix that was implimented is to see if there is an exclimation point, the character used to diferencate between an image and a link, in the file and, if it exists, if the exclimation point is in front of the brackets, which would be where it is placed if it is an image instead of a link. In this case, it would not be considered a link and thus not added to the return.

Passing the below file would test both of these cases.

[Bug Two](https://tcarman.github.io/cse15l-lab-reports/Bug-Two-Report2.html)

## Bug Three

![Bug Three](LabReport2SS3.png)

The final bug being covered here is the empty line bug. With the orginal code, an empty line would result in an infinate loop. This line makes sure all of the characters needed for a valid link, brackets [] and parenthesies (), are in the remainder of the document after the link has been added to the return list. Before adding this chunk, the code would spin, trying to find characters that did not exist, until it ran out of space and then return nothing, this short cuts that spinning by breaking the loop.

[Bug Three](https://tcarman.github.io/cse15l-lab-reports/Bug-Three-Report2.html)
