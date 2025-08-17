## access deined

$ git add . ; git commit -m "linux" ; git push origin main
On branch main
nothing to commit, working tree clean
remote: Permission to NagaLakshmi477/linux.git denied to lakshmireddy-77.
fatal: unable to access 'https://github.com/NagaLakshmi477/linux.git/': The requested URL returned error: 403


## solution

$ ls ~/.ssh
id_ed25519  id_ed25519.pub  known_hosts  known_hosts.old

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$ cat id_ed25519.pub
cat: id_ed25519.pub: No such file or directory

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$ cat ~/.ssh/id_ed25519.pub
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAICWTrWVqeVKkgC3VbEpzo0bgHTqa1OLs2QolLAShD6pS awsd851@gmail.com

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$ git add . ; git commit -m "git error " ; git push origin main
On branch main
nothing to commit, working tree clean
remote: Permission to NagaLakshmi477/errors.git denied to lakshmireddy-77.
fatal: unable to access 'https://github.com/NagaLakshmi477/errors.git/': The requested URL returned error: 403

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$ git add . ; git commit -m "git error " ; git push origin main
On branch main
nothing to commit, working tree clean
remote: Permission to NagaLakshmi477/errors.git denied to lakshmireddy-77.
fatal: unable to access 'https://github.com/NagaLakshmi477/errors.git/': The requested URL returned error: 403

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$ git remote set-url origin git@github.com:NagaLakshmi477/errors.git

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$ git remote -v
origin  git@github.com:NagaLakshmi477/errors.git (fetch)
origin  git@github.com:NagaLakshmi477/errors.git (push)

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$ ssh -T git@github.com
Hi NagaLakshmi477! You've successfully authenticated, but GitHub does not provide shell access.

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 242 bytes | 40.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:NagaLakshmi477/errors.git
 * [new branch]      main -> main

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/errors (main)
$ cd ..

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos
$ cd linux

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/linux (main)
$ git remote set-url origin git@github.com:NagaLakshmi477/linux.git

DELL@DESKTOP-LNC7QP1 MINGW64 ~/Documents/DevSecOps/repos/linux (main)
$ git push origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 7.71 KiB | 3.86 MiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:NagaLakshmi477/linux.git
 * [new branch]      main -> main
