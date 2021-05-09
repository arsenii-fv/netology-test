
$ git remote add main https://github.com/arsenii-fv/netology-test.git
$ git push -f main main 
$ mkdir branching
$ nano branching/merge.sh
$ nano branching/rebase.sh
$ git add branching/merge.sh branching/rebase.sh
$ git commit -a -m "Prepare for merge and rebase"
$ git checkout -b git-merge
$ nano branching/merge.sh
$ git commit -a -m "merge: @ instead *"
$ git push main git-merge
$ nano branching/merge.sh
$ git commit -a -m "merge: use shift"
$ git push main git-merge

$ git log --oneline
$ git checkout main
$ git log --oneline
$ nano branching/rebase.sh
$ git push main main
$ git commit -a -m "rebase: @ instead *"
$ git push main main
$ git log --oneline

$ git checkout 874fe23
$ git log --oneline
$ git checkout -b git-rebase
$ nano branching/rebase.sh
$ git commit -a -m "git-rebase 1"
$ nano branching/rebase.sh
$ git commit -a -m "git-rebase 2"
$ git push main main
$ git push main git-rebase
$ git log --oneline
$ git checkout main
$ git log --oneline
$ git merge git-merge
$ git push main main
$ git checkout git-rebase
$ git rebase -i main
$ git add branching/rebase.sh
$ git rebase --continue
$ nano branching/rebase.sh
$ git add branching/rebase.sh
$ git rebase --continue
$ git push -u main git-rebase
$ git push -u main git-rebase -f
$ git checkout main
$ git merge git-rebase

