---
layout: center
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
---

# Git branches

- Tot nu toe: lineare historie (vb. 1)
- Nieuwe situatie commit maken (vb. 2):
  1. Maak branch (aftakking) vanaf _main_
  2. Werk aan feature of bugfix
  3. Commit naar nieuwe branch
  4. Ga naar GitHub, maak een pull request:

::right::

```mermaid
---
title: Voorbeeld 1 - Historie met 1 branch (main)
---
gitGraph
   commit id: "Add stub README.md"
   commit id: "Add first parts of GUI"
   commit id: "Add some functionality"
   commit id: "Add build instructions to README.md"
```

```mermaid
---
title: Voorbeeld 2 - Historie met 3 branch (main, feature-1, feature-2)
---
gitGraph
  commit id: "Initial commit" tag: "v1.0"
  branch feature-1
  commit id: "Feature 1 - Commit 1"
  commit id: "Feature 1 - Commit 2"
  checkout main
  merge feature-1 tag: "Merge feature-1"

  branch feature-2
  commit id: "Feature 2 - Commit 1"
  commit id: "Feature 2 - Commit 2"
  commit id: "Feature 2 - Commit 3"
  checkout main
  merge feature-2 tag: "Merge feature-2"
```

---

# GitHub pull requests

---

# Merge conflicts
