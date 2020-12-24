##### Configure Beyond Compare 4 as a Diff (difference) tool  

Beyond Compare (BC) is a fabulous (in this authors' opinion) differencing and  
merge tool. It's inexpensive and works on just about anything (binary files,  
text, etc.)  
If the user decides to use BC for such purposes, below explains how to  
configure git to use BC as the preferred difference/merge tool.  
Perform this activity wherever BC is installed to ensure consistent operation.  

  * git config --global diff.tool bc  
  * git config --global difftool.bc.path "C:\Program Files\Beyond Compare 4\BCompare.exe"  
    * Ensure that the path is to your copy of BC.  
    * Ensure that, if there are spaces in the path, that the path is enclosed  
      in double quotes (").

##### To use BC as a difference tool

  * git difftool --dir-diff
    * This will compare the difference between the working directory and the  
      last fetch/pull.

##### Configure Beyond Compare as a Merge tool

  * git config --global merge.tool bc  
  * git config --global mergetool.bc.path "C:\Program Files\Beyond Compare 4\BCompare.exe"  

##### To use BC as a 3-way merge tool

  * git mergetool \<Some File Name\>

Gits default setting is to retain merge files with *.orig extensions after a  
successful merge. To disable this **_safety feature_** and automatically  
delete *.orig files after a merge, execute:

  * git config --global mergetool.keepBackup false

If you are presented with a prompt, e.g. "Launch 'bc4' [Y/n]?" when performing  
a diff and you do not wish to see said prompt, execute the following

  * git config --global difftool.prompt false  

and the prompt should not longer be displayed.  
