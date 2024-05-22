hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ history 
    1  git --version
    2  history 

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ 2
bash: 2: command not found

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git history
git: 'history' is not a git command. See 'git --help'.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log
commit 92eeb149fa4429de9f19d49249f06a1bc19b215a (HEAD -> main)        
Author: honey11badger <basiledembe@gmail.com>
Date:   Tue May 21 17:47:41 2024 +0200

    chore:create fourth file

commit 97c0a712180cfafdc2410d239c84690b7e27d619
Author: honey11badger <basiledembe@gmail.com>
Date:   Tue May 21 17:31:47 2024 +0200

    chore: Create third file

commit 33ea5ad274248fbfb9237b9af5382cad23865800
Author: honey11badger <basiledembe@gmail.com>
Date:   Tue May 21 17:27:47 2024 +0200

    chore: merged create second into create initial file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase
There is no tracking information for the current branch.
Please specify which branch you want to rebase against.
See git-rebase(1) for details.
pick 97c0a71 chore: Create third file
# This is a combination of 2 commits.

    git rebase '<branch>'

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=<remote>/<branch> main


hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
92eeb14 (HEAD -> main) chore:create fourth file
97c0a71 chore: Create third file
33ea5ad chore: merged create second into create initial file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~3
fatal: invalid upstream 'HEAD~3'

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~2
[detached HEAD 20d4f6a] chore: Create third and fourth file
 Date: Tue May 21 17:31:47 2024 +0200
 2 files changed, 1 insertion(+)
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
20d4f6a (HEAD -> main) chore: Create third and fourth file
33ea5ad chore: merged create second into create initial file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
pick 20d4f6a chore: Create third and fourth file
$ git add unwanted.txt

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git commit -m"unwanted commit"
[main 1f42a8c] unwanted commit
 1 file changed, 2 insertions(+)
 create mode 100644 unwanted.txt

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --online
fatal: unrecognized argument: --online

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
1f42a8c (HEAD -> main) unwanted commit
20d4f6a chore: Create third and fourth file
33ea5ad chore: merged create second into create initial file

noop
hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
20d4f6a (HEAD -> main) chore: Create third and fourth file
33ea5ad chore: merged create second into create initial file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~3
fatal: invalid upstream 'HEAD~3'

pick 20d4f6a chore: Create third and fourth file
hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~2
fatal: invalid upstream 'HEAD~2'

pick 20d4f6a chore: Create third and fourth file:
hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
20d4f6a (HEAD -> main) chore: Create third and fourth file
33ea5ad chore: merged create second into create initial file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase i HEAD~1
fatal: invalid upstream 'i'

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~1
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i --root
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
5aa1e21 (HEAD -> main) chore: merged create second into create initial file
5d6dd45 chore: Create third and fourth file
hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~3
fatal: invalid upstream 'HEAD~3'

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~2
[detached HEAD 20d4f6a] chore: Create third and fourth file
 Date: Tue May 21 17:31:47 2024 +0200
 2 files changed, 1 insertion(+)
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
20d4f6a (HEAD -> main) chore: Create third and fourth file
33ea5ad chore: merged create second into create initial file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
pick 20d4f6a chore: Create third and fourth file
$ git add unwanted.txt

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git commit -m"unwanted commit"
[main 1f42a8c] unwanted commit
 1 file changed, 2 insertions(+)
 create mode 100644 unwanted.txt

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --online
fatal: unrecognized argument: --online

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
1f42a8c (HEAD -> main) unwanted commit
20d4f6a chore: Create third and fourth file
33ea5ad chore: merged create second into create initial file

noop
hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
20d4f6a (HEAD -> main) chore: Create third and fourth file
33ea5ad chore: merged create second into create initial file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~3
fatal: invalid upstream 'HEAD~3'

pick 20d4f6a chore: Create third and fourth file
hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~2
fatal: invalid upstream 'HEAD~2'

pick 20d4f6a chore: Create third and fourth file:
hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
20d4f6a (HEAD -> main) chore: Create third and fourth file
33ea5ad chore: merged create second into create initial file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase i HEAD~1
fatal: invalid upstream 'i'

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i HEAD~1
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git rebase -i --root
Successfully rebased and updated refs/heads/main.

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
5aa1e21 (HEAD -> main) chore: merged create second into create initial file
5d6dd45 chore: Create third and fourth file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git checkout main
Already on 'main'

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git checkout -b ft/branch
Switched to a new branch 'ft/branch'

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (ft/branch)
$ git add test5.md

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (ft/branch)
$ git commit -m"Implemented test 5"
[ft/branch 88bb0d9] Implemented test 5
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (ft/branch)
$ git checkout main
Switched to branch 'main'

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log ft/branch --online 
fatal: unrecognized argument: --online

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log ft/branch --oneline
88bb0d9 (ft/branch) Implemented test 5
5aa1e21 (HEAD -> main) chore: merged create second into create initial file
5d6dd45 chore: Create third and fourth file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git checkout ft/branch
Switched to branch 'ft/branch'

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (ft/branch)
$ git log --oneline
88bb0d9 (HEAD -> ft/branch) Implemented test 5
5aa1e21 (main) chore: merged create second into create initial file   
5d6dd45 chore: Create third and fourth file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (ft/branch)
$ git checkout main
Switched to branch 'main'

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git cherry-pick 88bb0d9
[main d38ab39] Implemented test 5
 Date: Wed May 22 15:32:55 2024 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --oneline
d38ab39 (HEAD -> main) Implemented test 5
5aa1e21 chore: merged create second into create initial file
5d6dd45 chore: Create third and fourth file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git log --graph
* commit d38ab39003297b26bc1e24c0d029bc2a87905d58 (HEAD -> main)
| Author: honey11badger <basiledembe@gmail.com>
| Date:   Wed May 22 15:32:55 2024 +0200
|
|     Implemented test 5
|
* commit 5aa1e21c2456011fe0b87d676d3dc6cfbdbb02dc
| Author: honey11badger <basiledembe@gmail.com>
| Date:   Tue May 21 17:27:47 2024 +0200
|
|     chore: merged create second into create initial file
|
* commit 5d6dd455eba6692fde4687dbc5d73eb4022d0e67
  Author: honey11badger <basiledembe@gmail.com>
  Date:   Tue May 21 17:31:47 2024 +0200

      chore: Create third and fourth file

hp@DESKTOP-VLJO66J MINGW64 ~/Pictures/practice/Git Advanced Exercise (main)
$ git reflog 
d38ab39 (HEAD -> main) HEAD@{0}: cherry-pick: Implemented test 5
5aa1e21 HEAD@{1}: checkout: moving from ft/branch to main
88bb0d9 (ft/branch) HEAD@{2}: checkout: moving from main to ft/branch 
5aa1e21 HEAD@{3}: checkout: moving from ft/branch to main
88bb0d9 (ft/branch) HEAD@{4}: commit: Implemented test 5
5aa1e21 HEAD@{5}: checkout: moving from main to ft/branch
5aa1e21 HEAD@{6}: checkout: moving from main to main
5aa1e21 HEAD@{7}: rebase (finish): returning to refs/heads/main       
5aa1e21 HEAD@{8}: rebase (pick): chore: merged create second into create initial file
5d6dd45 HEAD@{9}: rebase (pick): chore: Create third and fourth file  
5e198c9 HEAD@{10}: rebase (start): checkout 5e198c9c2d5f20f0b1b19a4fa1c841271d87d3e3
20d4f6a HEAD@{11}: rebase (finish): returning to refs/heads/main      
20d4f6a HEAD@{12}: rebase (start): checkout HEAD~1
20d4f6a HEAD@{13}: rebase (finish): returning to refs/heads/main      
20d4f6a HEAD@{14}: rebase (start): checkout HEAD
20d4f6a HEAD@{15}: rebase (finish): returning to refs/heads/main      
20d4f6a HEAD@{16}: rebase (start): checkout HEAD~2
1f42a8c HEAD@{17}: commit: unwanted commit
20d4f6a HEAD@{18}: rebase (finish): returning to refs/heads/main      
20d4f6a HEAD@{19}: rebase (squash): chore: Create third and fourth file
97c0a71 HEAD@{20}: rebase (start): checkout HEAD~2
:
