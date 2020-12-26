---
{
  "Tags": 
  [
    "Git"
    , "Git-Flow"
    , "Visual Studio Code"
    , "VS Code"
    , "Beyond Compare"
  ]
  , "Date": "2020-12-21"  
  , "Author": "Bruce Lackore, Lead Engineer, Arizona Office of the Courts  "
  , "Software Versions":
    [
      "Git version 2.29.2.3"
      , "Beyond Compare 4.3.7, Build 25118"
    ] 
}
---

### Install, configure and perform basic activities using Git:

 1. Install Git for Windows 10  

 2. Configure Git for Windows 10  

 3. Create aliases for commonly used Git commands  

 4. Optionally configure Git to use Beyond Compare as a Diff/merge tool  

</b>

<details>
  <summary>Definitions</summary>

Version Control System.
  * Centralized - Essentially a centralized Version Control System (VCS) is  
    defined by it's requirement that all inputs be stored in a central location  
    on a purpose-designated server.  
    All users must communicate with the server to check changes in and obtain  
    the latest changes from their co-workers.

  * Distributed - A distributed VCS works as a community. Each user has  
    (potentially) a full copy of the work in progress and thus all versions  
    of the repository are equal in that if one member leaves the team, there  
    is no specific problem in that everyone else will have a full copy of the  
    repository.

</details>

<details>
  <summary>Goals</summary>

1. Install Git
2. Create Git aliases for commonly used commands
3. Explain the Git file structure from the 50,000 ft level
4. Demonstrate why Git is safe
5. Demonstrate branching and branch merging in Git
6. Show a usable, production-ready process for integrating Git into the  
   development process.

</details>

<details>
  <summary>Requirements</summary>

    1. Administrative access on the host.  
    2. A standardized location on the host to store local copies of repositories  
      a. A suggestion is Users\<Your user name>\Documents\_Repos

</details>

<details>
  <summary>Presumptions</summary>

    1.  Ability to open an administrative command prompt.  
    2.  Ability to open an administrative PowerShell prompt.  
    3.  Ability to cause the selected command shell to display hidden files  
        and/or directories.
 
</details>

<details>
  <summary>Software Needed</summary>

The following software should be obtained prior to beginning the installation  
and configuration process:  

   * [Visual Studio Code][VisualStudioCode-Url]  

     -- OR --  
   * [Visual Studio Code Insiders][VisualStudioCodeInsiders-Url]

   * [Git][Git-Url]  
   * [(Optional) Beyond Compare Diff/Merge tool][BeyondCompare-Url]

</details>

<details>
  <summary>Installation walk-through</summary>

[Installation Walk-through][GitConfigurationWalk-Through-Url]
</details>

### Post-Installation  

<details>
  <summary>Setting Git defaults</summary>

Execute the following commands to configure Git for your use:  

  * git config --system core.longpaths true
  * git config --global user.name "\<Your name\>"
  * git config --global user.email \<Your Email address\>
  * git config --global core.autocrlf input
    * This last command ensures "Commit as-is, pull as Unix".

</details>

<details>
  <summary>(Optional) Configure Git to use Beyond Compare 4 for Diff/Merge</summary>

[Configure Git to use Beyond Compare 4 for Diff/Merge][ConfigureGitBeyondCompare4-Url]

</details>  

<details>
  <summary>Make your life easier with Git command aliases</summary>

</details>

### Using Git

<details>
  <summary>Overview</summary>

### The core and basis of Git
The short version: "It's all about the working directory". What does that mean?  
Well, in short, the place where all your modifications should be taking place  
is in the working directory or a sub-directory of that working directory.  
Let's say you create a directory called "MyWebSite" and start writing code in  
that directory.  
In order for it to be a true Git "working directory", you need to turn that  
directory into a repository, this is done with a simple command that'll be  
described in the walk-through a little later in this document.  
The way that Git functions as a version control system is that, unlike some  
other VC systems, Git takes "snapshots", _not_ deltas of changes to the working  
directory.  
Think of it this way: Movies are, to the naked eye, a continuous flow of imagery  
that is seamless and smooth. If the movie is viewed in its raw state, one can  
see that rather than a continuous flow, the movie is actually a collection of  
snapshots of the activity being performed in front of the lense.  
What makes this collection of individual snapshots a "movie" is that the  
snapshots are presented to the naked eye so quickly that the eye cannot see the  
breaks between the individual snapshots (frames) (a phenomenon called  
"persistence of vision") and thus we think we see a continuous moving picture.  
Each snapshot contains all of the information available, e.g. the entire content  
of what the lense is looking at, and is copied and stored as a frame of picture.  
Moving to the next frame doesn't show just the parts that have moved (changed)  
since the last frame, the new frame contains all of the information in front  
of the lense _at the moment the frame was created_.  
In short, each snapshot contains everything the lense sees at the moment the  
frame was created. This is the same for Git. Whenever its asked to, it takes  
a "snapshot" of the entire content of the working directory and stores it for  
later processing.  

**This is the most important aspect of Git storage to understand - the entire  
repository is nothing more than a collection of snapshots of the working  
directory, each snapshot created independently and each reflecting the  
**_full_** content of the working directory at the time the snapshot was  
taken.**  

The other important concept to wrap your head around is that Git is a _file  
system_.  Much like your directories store items in hierarchal form, Git  
also stores it's working directory snapshots in a hierarchy. The details of  
the hierarchy are un-important for the average user, it's just necessary to  
understand the file system notion when dealing with branching and merging of  
snapshots.

</details>

<details>
  <summary>The "Three" States of a Git File</summary>

[The Three States][TheThreeStates-Url]  

</details>  

<details>
  <summary>A bit of fun with branching</summary>

[Fun with Branching][FunWithBranching-Url]

</details>  

<details>
  <summary>Scenarios</summary>

</details>  

### Resources

<details>
  <summary>Articles</summary>

[Setting up Git](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)  
[Configure Git to use Beyond Compare](http://www.scootersoftware.com/support.php?zz=kb_vcs)  
[GitFlow Workflow](https://www.gitflow.com/)  
["Pro Git", the free Book](https://git-scm.com/book/en/v2)  

</details>

<details>
  <summary>Software</summary>

[Git][Git-Url]  
[Visual Studio Code][VisualStudioCode-Url]  
[Visual Studio Code Insiders][VisualStudioCodeInsiders-Url]  
[(Optional) Beyond Compare Diff/Merge Tool][BeyondCompare-Url]

[Git-Url]: https://git-scm.com/downloads  
[VisualStudioCode-Url]: https://code.visualstudio.com/Download
[VisualStudioCodeInsiders-Url]: https://code.visualstudio.com/insiders/
[BeyondCompare-Url]: https://www.scootersoftware.com/download.php  

[GitConfigurationWalk-Through-Url]: chapters/GitInstallationWalk-Through.md
[ConfigureGitBeyondCompare4-Url]: chapters/ConfigureBeyondCompare4AsADiffAndMergeTool.md  
[TheThreeStates-Url]: chapters/TheThreeStatesOfAGitFile.md  
[FunWithBranching-Url]: chapters/ABitMoreFunWithGitBranching.md

</details>