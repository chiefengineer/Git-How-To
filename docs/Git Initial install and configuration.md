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
  * Centralized
  * Distributed  

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

    No special requirements.

</details>

<details>
  <summary>Presumptions</summary>

    No presumptions.

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
  <summary>Making your life easier with Git aliases</summary>

</details>

<details>
  <summary>(Optional) Configure Git to use Beyond Compare 4 for Diff/Merge</summary>

[Configure Git to use Beyond Compare 4 for Diff/Merge][ConfigureGitBeyondCompare4-Url]

</details>  

### Using Git

<details>
  <summary>Overview</summary>

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

[Git, the free Book](https://git-scm.com/book/en/v2)  

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

</details>