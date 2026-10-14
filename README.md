--create local repo then connect to remote repo
$ git init vc-lab2
$ git remote add origin https://github.com/emanibrahim0m/vc-iti-lab2.git

	touch gitcommand.txt
-- create first commit
$ git add .
$ git commit -m "First File"
$ git push -u origin main

--create dev branch (create commit - push - merge)
$ git branch dev
$ git switch Dev
	touch dev.txt
$ git add .
$ git commit -m "Dev Branch"
$ git checkout main
$ git push -u origin dev
$ git merge Dev

--create test branch (create commit - push - merge)
$ git branch Test
$ git switch Test
	touch Test.txt
$ git add .
$ git commit -m "Test Branch"
$ git checkout main
$ git push Test
$ git merge Test

-- delete branches from remote
git push origin --delete Test
git push origin --delete Dev

-- delete branches from local
git checkout main
git branch -d Test
git branch -d Dev

-- save changes in main without commit
$ git branch New
git stash
git checkout New
git stash pop

--create annotated tag
$ git tag -a v1.7 -m "Annotated tag"

-- push tag to remote repo
git push origin v1.7

--List tags
git tag

--delete tag locally
git tag -d v1.7

--delete tag Remotely
git push origin --delete v1.7



<img width="597" height="335" alt="images" src="https://github.com/user-attachments/assets/aa17f3c9-7af9-4e8d-8b7d-91e02c2382ae" />
