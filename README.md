
# PSPathFindir : Filesystem Navigation Simplified

***PSPathFindir*** is an incredibly simple solution to an incredibly basic problem. That being said, the question must be asked:

**Do YOU get tired of typing out paths when navigating your filesystem?  Wish there was a centralized place where you could store all your favorite paths in variables to ease traversing your directories?**

**MEET**: ***PSPathFindir***

***PathFIndir*** is a PowerShell Module which satisfies this need and with as little overhead as is possible! At it's core, PSPathFindir is merely a simple PowerShell Data File (*.psd1 extension), same as is used for Module Manifests, and as Configuration files for scripts, which contains a simple hashtable populated with user defined paths, and a central controller script which executes everything it needs to off of ***a single line of PowerShell Code.*** Make Filesystem traversal easy, with ***PSPathFindir!***

## How it Works

The **single line of code** mentioned above merely Imports the psd1 File containing PathFindir's *Path Index*, and stores the data from this file in a Variable called **'$Find'**. Trying to remember an important path? Simply execute **$Find**. Ready to change directories to a favorite Path? Simple as :

`cd $Find.MyFavoritePathName`

***Enough Said***

## Installation

`Install-Module PSPathFindir | Import-Module`

## Helper Functions

**Minimalism** is my middle name. Well, ***not really***, but it's a thing that people say, so I said it. In any case, PathFindir includes only the **BARE MINIMUM** in terms of Functions, or anything beyond the ***$Find*** Variable. These include:

* **New-PathIndexEntry** - Creates a new Key/Value pair within the PSPathFindir Path Index. (*Key* being the paths new 'nickname', *Value* being the actual path to the filesystem location.) Also accepts Objects as input, meaning you can create ***Multi-Level*** Keys, in essense, Path Aliases that contain multiple sub-paths. (*i.e. $Find.Projects.PowerShell, $Find.Projects.Python, $Find.Projects.EnglishLit*)

* **Remove-PathIndexEntry** - Removes the specified Key/Value pair from the Path Index.

* **Get-PathIndexEntry** - Returns the entire Path Index contents by default, or the value of a specific Key if an argument is supplied to the '-Name' Parameter.

## Conclusion

**You should install PSPathFindir TODAY!**
