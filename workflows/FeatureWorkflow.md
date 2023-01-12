## Feature Workflow

- open **Feature Branch**
  - review/cleanup: log (validity); repo, branches(`gsb`) and stashes
  - ***Update Branches***
  - create new feature branch | or | open existing branch
  - push: `push --upstream origin <wb>`<br/><br/>

- until **Branch** work complete {

  - until **push Main** {

    - until **merge to Main** {<br><br><br>

      - while **push branch** {
        - ***Update Branches***
        - verify matching active branch
        - while **commit** {
          - while **stage** { develop; test } **stage**
          - ~~Inspect~~
          - show staged changes `diff --staged`<br>
        - } **commit |** verify target branch; commit changes
        - `glgr`; verify target branch; rebase if indicated `git rebase -i`
      - } **push branch |** on &lt;wb&gt;: `git push`<br><br><br><br>

    - } **merge to `main`** *merge &lt;wb&gt; into main line of development*
      - ***Update Branches***
      - checkout &lt;wb&gt;; `gsb`: review repo, branches, status
      - *preview merge*: `difftool main`
    - } **merge |** `checkout main; merge --edit --no-ff <wb>`<br><br>
  - } **push main |** on `main`: `git push`<br><br>

- } **Branch**

#### Update Branches
- `gsb`: review git repo, branches, status
- checkout main; fetch --prune
- if changes:
  - *update local main with fetched changes*
  - *verify local and remote main now match*: `diff main origin/main`
  - *update local and remote &lt;wb&gt; from main*:
    - `checkout <wb>; difftool main; merge --edit --no-ff main; push`
  - checkout main

<button onclick="window.print()">Print Button</button>
