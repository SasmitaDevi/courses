---
layout: exercise
title: Version Control 7
---

This is a follow up question to
[Version Control 6]({{ site.github.url }}/exercises/Version-control-6).

You and your team member decide to split up the work that needs to be done. You should
each work in your own local clone of the repository, then share the resulting files by 
committing them and pushing them to GitHub. 

The six data files required for the project are available from `{{ site.github.url }}/data`
and are called `areas1.txt` througn `areas6.txt`. One team member should download all of 
these files using the `curl` command, commit them to their repository, and push to GitHub.

While the first team member is downloading the data files, the second team member
can work on a script that will run the data files through the Python code and produce 
a single list of the areas and associated richness predictions from all of the sites 
combined. This list should be sorted from the smallest area to the largest area, 
and should only include unique values.You could 
cut and paste the files together, run them through the Python code, and then 
do some post processing to get the list looking right, but new files are going 
to be showing up constantly, and besides, this can be readily accomplished in 
one line using the shell. You could use a loop, but since you just need a 
single list of areas and predictions it's probably easier to just use `cat` 
to concatenate all of the files at the beginning. Once you've figured out the 
necessary shell commands put them in a text file and save it as `predict_richness.sh`. 
Since you'll need the data files to test the script, you'll have to wait until your
team member lets you know they have been committed to GitHub. Then you can update
your local repository to obtain the files. Test to make sure everything is working 
by running the script using the command `bash predict_richness.sh`. Commit the 
`predict_richness.sh` script to the local repository and push to GitHub.

Once the script has been made available on GitHub, the first team member should 
update their repository and run the script. The results should be saved in a file called
`predicted_diversities.txt`, committed to their local repository, and pushed to GitHub.
