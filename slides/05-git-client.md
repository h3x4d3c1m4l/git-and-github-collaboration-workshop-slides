---
layout: figure-side
figureUrl: img/vs-code/clients.png
figureCaption: Overzicht van Git clients.
figureFootnoteNumber: 1
---

# Git clients

- Veel verschillende clients
  - GitHub Desktop
  - Sourcetree
  - Fork
  - Visual Studio (Code)
  - JetBrains WebStorm, PyCharm, ...
- Standaard operaties kunnen ze allemaal
- We zoomen in op Visual Studio Code

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/downloads/guis" rel="noreferrer" target="_blank">https://git-scm.com/downloads/guis</a></Footnote>
</Footnotes>

---
layout: figure
transition: fade
figureUrl: img/vs-code/clone.png
figureCaption: Gebruik het command menu (F1) om te clonen.
---

# VS Code - Clone

---
layout: figure-side
transition: fade
figureUrl: img/vs-code/clone-from-url.png
figureCaption: Kies de repository die je wil clonen.
---

# VS Code - Clone

- Log in bij GitHub en kies de repository of kopieer de URL uit je browser
- Kies de map waar de repository gecloned mag worden
  - Daar binnen wordt een *nieuwe* map gemaakt
  - Kies een map die je terug kunt vinden (bv. Documenten)
- De _remote repo_ wordt nu gedownload naar een _local repo_
- Er wordt een automatisch _checkout_ van de _main_ branch uitgevoerd

---
layout: figure-side
transition: fade
figureUrl: img/vs-code/pre-stage.png
figureCaption: Stage een deel, of stage in 1 keer alles.
---

# VS Code - Stage

- Stappen:
  1. Je maakt wijzigingen
      - Maak, wijzig of wis bestanden
  2. Open VS Code, tabje _Source Control_
  3. Loop je wijzigingen na
  4. _Stage_ de wijzigingen die je wil meenemen
      - De wijzigingen staan nu in de _staging area_

---
layout: figure-side
transition: fade
figureUrl: img/vs-code/post-stage.png
figureCaption: Alles gestaged en de commit message geschreven? Klaar om te committen.
---

# VS Code - Commit

- Stappen:
  1. Je maakt wijzigingen
      - Maak, wijzig of wis bestanden
  2. Open VS Code, tabje _Source Control_
  3. Loop je wijzigingen na
  4. _Stage_ de wijzigingen die je wil meenemen
      - De wijzigingen staan nu in de _staging area_
  5. Geef je wijzigingen een *duidelijke* omschrijving en klik op _✓ Commit_
     - De commit staat nu in je _local repo_

---
layout: figure-side
figureUrl: img/vs-code/sync-changes.png
---

# VS Code - Push

- Stappen:
  1. Je maakt wijzigingen
      - Maak, wijzig of wis bestanden
  2. Open VS Code, tabje _Source Control_
  3. Loop je wijzigingen na
  4. _Stage_ de wijzigingen die je wil meenemen
     - De wijzigingen staan nu in de _staging area_
  5. Geef je wijzigingen een *duidelijke* omschrijving en klik op _✓ Commit_
     - De commit staat nu in je _local repo_
  6. Klik op _Sync Changes 1↑_
     - De commit staat nu in je _remote repo_
