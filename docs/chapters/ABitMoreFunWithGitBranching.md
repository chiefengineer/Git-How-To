### A bit of fun with git branching

  1.  We will presume that the repository created via the above process still  
      exists. If not, please go re-create it.
  2.  Now, to create a branch, execute the following command:
        `git branch Toy`

      This creates a branch in the "Playground" repository called "Toy".
  3.  Do a directory and you will see that the content of the working directory  
      _is unchanged!_
      All that took place here is that Git was told to create a new  
      "sub-directory" if you will, in its own little file system.
  4.  Now, for Git to point that branch at your _working directory_, you need  
      to execute this command:

      `git checkout Toy`  
      
      You should see output similar to this:
      ```
      Switched to branch 'Toy'
      ```
  5.  Again, perform a directory list (`dir`) or (`ls`) and observe that your  
      file is still there, even though Git is now pointing to a different  
      branch. 
      Now, a bit of subtlety here. When you created your "Toy" branch, Git  
      privately took a snapshot of your current working directory and made  
      that it's first "commit". Why is this important?  
      Simple. When you change branches, you need to make **_ABSOLUTELY SURE  
      THAT THERE ARE NO PENDING CHANGES IN YOUR WORKING DIRECTORY!_**  
      What does this mean? No "open" files, all editing completed, all editors  
      saved, all changes written, nothing pending. Stage all your files (or  
      stash them, more about that later) and commit the changes.  
      Why, you might ask? Because when Git does a checkout, it writes the  
      current snapshot of the branch you are pointing at **to your working  
      directory** thus any changes you might have had would be otherwise lost.  
      Git is real good about warning you and even preventing you from doing  
      something monumentally stupid but the key here is that the snapshot  
      pointed to by the current branch is what your working directory will  
      look like when the checkout is complete.  
      There is, of course, **much** more to branching (and merging) than what  
      is described herein. This paper will not attempt to delve into all the  
      intricacies of branching and merging, rather simply give exposure to the  
      process and leave the rest of the research to the student.  
  6.  How to verify this? Open the file in your editor and add the following  
      text: "...this was done in the "Toy" branch." and save the file.
  7.  Stage the file and commit it: (`git add *` followed by `git commit`) if  
      you forgot.
  8.  Now, perform a `git checkout main`. Again, you should see a message  
      similar to:  
      ```
      Switched to branch 'main'  
      ```  
  9.  Now, the fun part. Open your file and observe that your change made  
      when in the "Toy" branch **_is gone_**!  
      Close the editor.
  10. Not to worry, execute the following command:  

      `git checkout Toy`  
  
      to switch back to the "Toy" branch.
  11. Open the file in your editor and viola! your change is back! Close the  
      editor.  
  12. Now, just to be sure we aren't lost, change back to the "main" branch:  
  
      `git checkout main`.  
  
      That, in a nutshell, is Git branching. Obviously this is a powerful tool  
      and much more investigation needs to be performed so this paper leaves  
      said investigation as "an exercise for the student".  
      There will be more examples of branching and merging in this paper in the  
      section titled "process".  
