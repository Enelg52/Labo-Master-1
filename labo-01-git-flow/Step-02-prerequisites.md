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
[INPUT]
winget install git.git
```

* [ ] Confirm the installed version

```
[INPUT]
git flow version

[OUTPUT]
1.12.3 (AVH Edition)
```

* [ ] What do you think about this release?

```
Ajout de l'option --noedit. 

Il s'agit d'une pull request de luiscoms
https://github.com/petervanderdoes/gitflow-avh/pull/338
```

## What's git-flow, branches feature.

[Source](https://nvie.com/posts/a-successful-git-branching-model/)

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Source : A successful git branching model</p></figcaption></figure>

* [ ] Which branches are persistent and what do they contain?

```
La branch main/master et develop.
Develop -> branch stable
Main -> Branch stable
```

* [ ] Why do we have to merge hotfix in both master and develop branches, but not into all active feature branches?

```
Un hotfix est par définition une correction en cours de route, donc il faut aussi corriger la branch stable. 
```

## Initialize git flow on an existing project

* [ ] What happens when you run the "git flow init" command on an existing local repository?

```
Ça créer la branch develop et ça switch dessus. 
```

* [ ] When do we need to make this git command?

```
Juste après avoir pull un repo. 
```

## Practice the basic git commands

[Source](https://www.atlassian.com/git/glossary)

* [ ] What does this git command "git add -all" achieve (.gitignore impacts)?

```
Ajouter tout les fichiers, sauf ceux spéfifié dans dans le .gitignore 
```

* [ ] What does this git command "git status" achieve?

```
Permets de voir l'état actuel de notre branch. 
```

* [ ] What does this git command "git remote add upstream \<url>" achieve?

```
Ajoute un autre remote. Permet de pull/push vers un autre repo que l'origin
```
