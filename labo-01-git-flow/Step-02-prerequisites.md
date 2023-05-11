# Prerequisites

## Setting up/updating the git environment and git flow

[Get the installer](https://git-scm.com/downloads)

{% hint style="info" %}
Git-flow library:\
For Windows, is natively integrated.\
For Mac, [here is the procedure](https://git-scm.com/download/mac).\
Pour Linux, [here is the procedure.](https://howtoinstall.co/en/git-flow)
{% endhint %}

```
I use Windows 11 version 22H2 so it's natively integrated
```

* [ ] Confirm the installed version

```
PS C:\Users\Ilan> git flow version
1.12.3 (AVH Edition)
PS C:\Users\Ilan>
```

* [ ] What do you think about this release?

```
Quoted form the git repo

This fork adds functionality not added to the original branch.

source:
https://github.com/petervanderdoes/gitflow-avh
```

## What's git-flow, branches feature.

[Source](https://nvie.com/posts/a-successful-git-branching-model/)

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Source : A successful git branching model</p></figcaption></figure>

* [ ] Which branches are persistent and what do they contain?

```
The branches named "main" and "develop".
The main branche is where the stable versions of the project are.
The develop branche is where the project's in developpement, it's there that new features are set.
```

* [ ] Why do we have to merge hotfix in both master and develop branches, but not into all active feature branches?

```
Because it's a "hotfix", which means that it correct some issues. This correction need to be applied in both branches, otherwise one will have the correction and the other one not. If so, it will cause a lot of collisions issues later on
```

## Initialize git flow on an existing project

* [ ] What happens when you run the "git flow init" command on an existing local repository?

```
It will open a prompt asking the name of the production branch, the development branches and others.
leave it empty to apply the default name
```

* [ ] When do we need to make this git command?

```
Right after the clonning of our git repo
```

## Practice the basic git commands

[Source](https://www.atlassian.com/git/glossary)

* [ ] What does this git command "git add -all" achieve (.gitignore impacts)?

```
It updates the index on the working tree and whre the index already has and entry. This command allows to add, modify and remove one or multiple index entries.


If the file is in the ".gitignore", it won't update the index for this file.

Source:
https://git-scm.com/docs/git-add
```

* [ ] What does this git command "git status" achieve?

```
It shows you if there are staged files in the current branch
```

* [ ] What does this git command "git remote add upstream \<url>" achieve?

```
It adds a new remote named "upstream" that points to the url.
```
