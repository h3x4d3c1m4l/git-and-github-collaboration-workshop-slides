---
layout: center
transition: fade
class: "text-center"
---

# Git branches

<span class="font-extralight">
  <q>Branching means you diverge from the main line of development and continue to do work without messing with that main line.</q>
  <sup>1</sup>
</span>

<Footnotes separator>
  <Footnote :number=1>Bron: <a href="https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell">git-scm.com</a></Footnote>
</Footnotes>

---
layout: two-cols
transition: fade
---

# Git branches

- Tot nu toe: lineare historie (vb. 1)
- Nieuwe situatie commit maken (vb. 2):
  - Verboden naar _main_ te committen, wat wel:
    1. Maak branch (aftakking) vanaf _main_
    2. Werk aan feature of bugfix
    3. Commit en push naar nieuwe branch
    4. Merge via pull request
    5. Rinse & repeat
- Pull request: Verzoek om een branch te mergen in een andere branch
  - Oftewel: De wijzigingen van een branch A bij een branch B te voegen
  - Voorbeeld: _feature-1_ naar _main_

::right::

```mermaid
---
title: Voorbeeld 1 - Historie met 1 branch (main)
---
gitGraph
   commit id: "Add stub README.md"
   commit id: "Add first parts of GUI"
   commit id: "Add some business logic"
   commit id: "Add build instructions to README.md"
```

```mermaid
---
title: Voorbeeld 2 - Historie met 3 branch (main, feature-1, feature-2)
---
gitGraph
  commit id: "Initial commit"
  branch feature-1
  commit id: "Feature 1 - Commit 1"
  commit id: "Feature 1 - Commit 2"
  checkout main
  merge feature-1 id: "Merge feature-1"

  branch feature-2
  commit id: "Feature 2 - Commit 1"
  commit id: "Feature 2 - Commit 2"
  commit id: "Feature 2 - Commit 3"
  checkout main
```


---
transition: fade
---

# Git branches - VS Code

![alt text](/img/branches-and-prs/vscode-create-branch.png)

![alt text](/img/branches-and-prs/vscode-checkout-branch.png)

---
layout: figure
transition: fade
figureUrl: img/branches-and-prs/pull-requests.png
figureCaption: De pull requests pagina van GitHub.
---

# GitHub pull requests

---
layout: figure
transition: fade
figureUrl: img/branches-and-prs/create-pull-requests.png
figureCaption: Zorg voor een beschrijvende titel en omschrijving en maak de pull request.
---

# GitHub pull requests

---
layout: two-cols
transition: fade
---

# Merge conflicts

![alt text](/img/branches-and-prs/merge-conflicts.png)

- Conflicterende wijzigingen uit 2 branches
- Komt o.a. door:
  - Zelfde line(s) gewijzigd
  - Branch 1: File verwijderd/hernoemd<br>Branch 2: File gewijzigd

::right::

```mermaid
---
title: Voorbeeld - Merge Conflict
---
gitGraph
  commit id: "Initial commit"
  branch feature-1
  commit id: "Feature 1 - Wijzig regel X"
  checkout main
  branch feature-2
  commit id: "Feature 2 - Ook wijziging in regel X"
  checkout main
  merge feature-1 id: "Merge feature-1"
```
