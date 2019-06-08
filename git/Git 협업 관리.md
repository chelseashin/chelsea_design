## Git 협업 관리

* terminal에서 실행

```python

student@DESKTOP MINGW64 /
$ git config --global --list
color.ui=true
user.name=chelseashin
user.email=chaewonshin95@gmail.com

student@DESKTOP MINGW64 /
$ cd ~ Desk
bash: cd: too many arguments

student@DESKTOP MINGW64 /
$ cd ~

student@DESKTOP MINGW64 ~
$ cd Desktop/

student@DESKTOP MINGW64 ~/Desktop
$ mkdir git-test

student@DESKTOP MINGW64 ~/Desktop
$ cd git-test/

student@DESKTOP MINGW64 ~/Desktop/git-test
$ git init
Initialized empty Git repository in C:/Users/student/Desktop/git-test/.git/

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ vi s1.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        s1.txt

nothing added to commit but untracked files present (use "git add" to track)

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git add s1.txt
warning: LF will be replaced by CRLF in s1.txt.
The file will have its original line endings in your working directory

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   s1.txt


student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git commit -m"11"
[master (root-commit) 477d585] 11
 1 file changed, 3 insertions(+)
 create mode 100644 s1.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log
commit 477d5852cf2e2f4c3aa46b7571fc238e35f535ca (HEAD -> master)
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:29:06 2019 +0900

    11

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ vi s1.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git add .
warning: LF will be replaced by CRLF in s1.txt.
The file will have its original line endings in your working directory

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git commit -m "22"
[master 2b2ae4e] 22
 1 file changed, 2 insertions(+), 2 deletions(-)

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log
commit 2b2ae4e711577fbf27396bcc12a8c56e0519a793 (HEAD -> master)
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:29:46 2019 +0900

    22

commit 477d5852cf2e2f4c3aa46b7571fc238e35f535ca
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:29:06 2019 +0900

    11

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git branch
* master

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git branch chel

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git branch
  chel
* master

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git checkout chel
Switched to branch 'chel'

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ ls
s1.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ cat s1.txt
a
b
c

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ vi s1.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ git add .
warning: LF will be replaced by CRLF in s1.txt.
The file will have its original line endings in your working directory

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ git commit -m "33"
[chel 2a6ea65] 33
 1 file changed, 2 insertions(+)

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ git log
commit 2a6ea650eaa5c0a5e7903b3c5b7df9a7697513b3 (HEAD -> chel)
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:32:16 2019 +0900

    33

commit 2b2ae4e711577fbf27396bcc12a8c56e0519a793 (master)
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:29:46 2019 +0900

    22

commit 477d5852cf2e2f4c3aa46b7571fc238e35f535ca
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:29:06 2019 +0900

    11

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ vi s2.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ git add
Nothing specified, nothing added.
Maybe you wanted to say 'git add .'?

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ git add .
warning: LF will be replaced by CRLF in s2.txt.
The file will have its original line endings in your working directory

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ git commit -m"44"
[chel 30f4ced] 44
 1 file changed, 5 insertions(+)
 create mode 100644 s2.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ git checkout master
Switched to branch 'master'

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log --branches
commit 30f4ced5937e4924b7a2e66004b9bf7ba2c3c94d (chel)
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:34:56 2019 +0900

    44

commit 2a6ea650eaa5c0a5e7903b3c5b7df9a7697513b3
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:32:16 2019 +0900

    33

commit 2b2ae4e711577fbf27396bcc12a8c56e0519a793 (HEAD -> master)
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:29:46 2019 +0900

    22

commit 477d5852cf2e2f4c3aa46b7571fc238e35f535ca
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:29:06 2019 +0900

    11

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log --branches --graph
* commit 30f4ced5937e4924b7a2e66004b9bf7ba2c3c94d (chel)
| Author: chelseashin <chaewonshin95@gmail.com>
| Date:   Tue May 14 10:34:56 2019 +0900
|
|     44
|
* commit 2a6ea650eaa5c0a5e7903b3c5b7df9a7697513b3
| Author: chelseashin <chaewonshin95@gmail.com>
| Date:   Tue May 14 10:32:16 2019 +0900
|
|     33
|
* commit 2b2ae4e711577fbf27396bcc12a8c56e0519a793 (HEAD -> master)
| Author: chelseashin <chaewonshin95@gmail.com>
| Date:   Tue May 14 10:29:46 2019 +0900
|
|     22
|
* commit 477d5852cf2e2f4c3aa46b7571fc238e35f535ca
  Author: chelseashin <chaewonshin95@gmail.com>
  Date:   Tue May 14 10:29:06 2019 +0900

      11

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log --branches --graph --oneline
* 30f4ced (chel) 44
* 2a6ea65 33
* 2b2ae4e (HEAD -> master) 22
* 477d585 11


student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ vi s3.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git add .
warning: LF will be replaced by CRLF in s3.txt.
The file will have its original line endings in your working directory

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git commit -m "55"
[master bbcb7dd] 55
 1 file changed, 1 insertion(+)
 create mode 100644 s3.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log --branches --graph --oneline
* bbcb7dd (HEAD -> master) 55
| * 30f4ced (chel) 44
| * 2a6ea65 33
|/
* 2b2ae4e 22
* 477d585 11

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log master..chel
commit 30f4ced5937e4924b7a2e66004b9bf7ba2c3c94d (chel)
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:34:56 2019 +0900

    44

commit 2a6ea650eaa5c0a5e7903b3c5b7df9a7697513b3
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:32:16 2019 +0900

    33

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log chel..master
commit bbcb7dd4d7d03034346e3590021d9ab1f9c220ed (HEAD -> master)
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:40:51 2019 +0900

    55

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log -p master..chel
commit 30f4ced5937e4924b7a2e66004b9bf7ba2c3c94d (chel)
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:34:56 2019 +0900

    44

diff --git a/s2.txt b/s2.txt
new file mode 100644
index 0000000..cd34a3c
--- /dev/null
+++ b/s2.txt
@@ -0,0 +1,5 @@
+1
+2
+31
+2
+3

commit 2a6ea650eaa5c0a5e7903b3c5b7df9a7697513b3
Author: chelseashin <chaewonshin95@gmail.com>
Date:   Tue May 14 10:32:16 2019 +0900

    33

diff --git a/s1.txt b/s1.txt
index de98044..2a2312d 100644
--- a/s1.txt
+++ b/s1.txt
@@ -1,3 +1,5 @@
 a
 b
 c
+e
+f

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git merge chel
Merge made by the 'recursive' strategy.
 s1.txt | 2 ++
 s2.txt | 5 +++++
 2 files changed, 7 insertions(+)
 create mode 100644 s2.txt

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log --branches --graph --oneline
*   44d3ee0 (HEAD -> master) Merge branch 'chel'
|\
| * 30f4ced (chel) 44
| * 2a6ea65 33
* | bbcb7dd 55
|/
* 2b2ae4e 22
* 477d585 11

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git checkout chel
Switched to branch 'chel'

student@DESKTOP MINGW64 ~/Desktop/git-test (chel)
$ git checkout master
Switched to branch 'master'

student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git branch -d chel
Deleted branch chel (was 30f4ced).

# 확인
student@DESKTOP MINGW64 ~/Desktop/git-test (master)
$ git log --branches --graph --oneline
*   44d3ee0 (HEAD -> master) Merge branch 'chel'
|\
| * 30f4ced 44
| * 2a6ea65 33
* | bbcb7dd 55
|/
* 2b2ae4e 22
* 477d585 11


```





### merge의 두가지 방식

1. ##### fastforward

   브랜치가 생성된 이후 마스터에 변경이 없을 때

   마스터가 가리키는 커밋을 브랜치가 가리키는 커밋으로 빨리감기

   별도의 커밋을 생성하지 않습니다.

2. ##### recursive

   브랜치가 마스터로 독립한 이후에 변화가 생긴 경우

   마스터와 브랜치의 공동의 부모커밋을 찾음

   3way merge  내부적인 방법으로 두 커밋을 합치고 별도의 merge commit을 생성함



##### git협업

1. 하나의 레포지토리
2. 두 개 이상의 레포지토리(소규모 대규모 오픈소스 기여)
  Collapse