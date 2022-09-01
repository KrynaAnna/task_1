# VC

kryna@DESKTOP-9TSFVTJ MINGW64 ~
$ cd Documents

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents
$ git config --global user.name "Anna_Kryna"

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents
$ git config --global user.email "krynaann13@gmail.com"

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents
$ git clone https://github.com/DataGlacier/VC.git
Cloning into 'VC'...
remote: Enumerating objects: 60, done.
Receiving objects: remote: Total 60 (delta 0), reused 0 (delta 0), pack-reused 60
Receiving objects: 100% (60/60), 14.27 KiB | 1.19 MiB/s, done.
Resolving deltas: 100% (18/18), done.

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents
$ cd VC

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (main)
$ ls
README.md  environment.yml  requirements.txt  response.json  scripts/  test/

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (main)
$ git branch new_branch

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (main)
$ git checkout new_branch
Switched to branch 'new_branch'

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (new_branch)
$ git status
On branch new_branch
nothing to commit, working tree clean

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (new_branch)
$ python add.py
C:\Users\kryna\AppData\Local\Programs\Python\Python310\python.exe: can't open file 'C:\\Users\\kryna\\Documents\\VC\\add.py': [Errno 2] No such file or directory

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (new_branch)
$ python scripts/add.py
Please add your name: Anna
Please add your favourite sports name: Tennis
Please add your name: Anna
Please add your favourite sports name: Tennis

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (new_branch)
$ pytest test/test.py -s
============================= test session starts =============================
platform win32 -- Python 3.9.7, pytest-7.1.1, pluggy-1.0.0
rootdir: C:\Users\kryna\Documents\VC
Please add your name: Anna
Please add your favourite sports name: Tennis
collected 1 item

test\test.py .

============================= 1 passed in 17.93s ==============================

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (new_branch)
$ git init
Reinitialized existing Git repository in C:/Users/kryna/Documents/VC/.git/

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (new_branch)
$ git add -A

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (new_branch)
$ git status
On branch new_branch
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   response.json


kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (new_branch)
$ git commit -m "First commit"
[new_branch 89f6584] First commit
 1 file changed, 3 insertions(+), 2 deletions(-)

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (new_branch)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (main)
$ git merge new_branch
Updating 9705c71..89f6584
Fast-forward
 response.json | 5 +++--
 1 file changed, 3 insertions(+), 2 deletions(-)

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (main)
$ git push https://github.com/KrynaAnna/task_1.git main
Enumerating objects: 63, done.
Counting objects: 100% (63/63), done.
Delta compression using up to 8 threads
Compressing objects: 100% (35/35), done.
Writing objects: 100% (63/63), 14.32 KiB | 3.58 MiB/s, done.
Total 63 (delta 20), reused 58 (delta 18), pack-reused 0
remote: Resolving deltas: 100% (20/20), done.
To https://github.com/KrynaAnna/task_1.git
 * [new branch]      main -> main

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (main)
$ git show-branch
* [main] First commit
 ! [new_branch] First commit
--
*+ [main] First commit

kryna@DESKTOP-9TSFVTJ MINGW64 ~/Documents/VC (main)
