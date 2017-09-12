# Our Songs
A repo is created for students to practice working with Git Remotes.

## recycle-bin folder
You can add/delete/revise any files to this folder. This is the playground for you to practice.

## Instructions for Assignment

1. Fork https://github.com/udmis/our-songs to your account.
2. Clone your forked repo, e.g, `git clone https://github.com/yourname/our-songs.git`
3. Go to your local folder "our-songs" and check your remote settings:
```
$ git remote -v
origin	https://github.com/harrywang/our-songs.git (fetch)
origin	https://github.com/harrywang/our-songs.git (push)
```
4. Add https://github.com/udmis/our-songs as your upstream remote:
```
$ git remote add upstream https://github.com/udmis/our-songs
$ git remote -v
origin	https://github.com/yourname/our-songs.git (fetch)
origin	https://github.com/yourname/our-songs.git (push)
upstream	https://github.com/udmis/our-songs (fetch)
upstream	https://github.com/udmis/our-songs (push)
```
5. Check your local branches
```
$ git branch
master
```
6. Create a new branch so that you can add your code to the repo:
```
$ git checkout -b harry-wang
Switched to a new branch 'harry-wang'
$ git branch
harry-wang
master
```
7. Now, create a folder with your full name (all lowercase, no spaces, use hyphen between your first and last name), e.g., harry-wang and create a html file to show the title, artist, and lyrics of a song of your choice. (see an example in my folder)
8. Commit the changes to the local branch:
```
$ git add *
$ git commit -am 'added a song'
[harry-wang 5534235] added a song
 3 files changed, 54 insertions(+), 2 deletions(-)
 rewrite README.md (100%)
 create mode 100644 harry-wang/img/sailing-to-philadelphia.jpg
 create mode 100644 harry-wang/sailing-to-philly.html
 ```
9. Merge yoru new branch to your master branch and delete the branch:
```
$ git checkout master
$ git merge harry-wang -m "merge my new song"
$ git branch -d harry-wang
```
10. Push your local changes to your forked repo:
```
$ git push origin master
```
11. Go to Github and issue a Pull Request (PR) so that the Admin of the "upstream" repo can review and merge your code:
<img width="1072" alt="screen shot 2017-09-12 at 11 16 00 am" src="https://user-images.githubusercontent.com/595772/30334273-109130aa-97ad-11e7-860c-dc2245f56b38.png">
<img width="1047" alt="screen shot 2017-09-12 at 11 16 29 am" src="https://user-images.githubusercontent.com/595772/30333903-17c8e12a-97ac-11e7-84d3-eca58dcbc12c.png">
<img width="801" alt="screen shot 2017-09-12 at 11 17 16 am" src="https://user-images.githubusercontent.com/595772/30333907-1ace7c04-97ac-11e7-9034-071ad1b0de00.png">
<img width="813" alt="screen shot 2017-09-12 at 11 17 26 am" src="https://user-images.githubusercontent.com/595772/30333912-1c635396-97ac-11e7-8921-c92a7718719e.png">


12. Once the change is merged by the upstream admin, you should switch back to the local master branch, pull the changes from the upstream repo and push the changes to your forked repo:

```
$ git checkout master
$ git pull upstream master
$ git push origin master
```

Congratulations, you just finished your first Github Workflow Exercise!
