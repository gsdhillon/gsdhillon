# Install Git on Windows 11

### Download Git64.exe and install [All Default Settings]


# Generated SSH Key on Windows 11

 ### Ringh click in D:\  > Show more options >  Git Bash Here
```
$ ssh-keygen -t ed25519 -C "gsdhillon@gmail.com"
Enter file in which to save the key (/c/Users/Ishjyot/.ssh/id_ed25519):   [Enter]
[Enter]
[Enter]
$ eval "$(ssh-agent -s)"
Agent pid 1147
$ ssh-add ~/.ssh/id_ed25519
Identity added: /c/Users/Ishjyot/.ssh/id_ed25519 (gsdhillon@gmail.com)
$ cd ~/.ssh/
$ cat id_ed25519.pub
```
### Registered public key on Github

* gsdhillon > Settings > SSH PGP Keys >  Add SSH Key >  Paste content of ~/.ssh/id_ed25519.pub
* 


# Generated SSH Key at Circle PC - Ubuntu 22.04
```
$ cd ~/.ssh
$ ls
$ ssh-keygen -o
Enter file in which to save the key (/home/gurmeet/.ssh/id_rsa): git_key_rsa
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in git_key_rsa
Your public key has been saved in git_key_rsa.pub
The key fingerprint is:
SHA256:/Uv/LaozGObWT4y2c+KYSUU5y4wYfirmRVRtY9DxOGA gurmeet@g
The key's randomart image is:
+---[RSA 3072]----+
|        E+..     |
|       o .*+     |
|      o  o*..    |
|     o o * +     |
|      + S *      |
|     . oo. +     |
|    o oo.+o =    |
|   o o .+=*+.o. .|
|    .  .+.+O+..oo|
+----[SHA256]-----+
$ cat ~/.ssh/git_key_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCsAzefobWPcF1CK60T7kT0jCMNHsaG9Itsu8l51+T1iH6BQdM+NInodgi8Kl4dClkU13IR3FtuGDBYxrSUw6pL/eFJSXG3rZSs5CweBZioiz0rozQsBLGopOTw/2lX//ELgRNglgXiF/K56iYcBYK6+ML4JbagZO82Bnve2NPfrMryBLv1eZWvrqEJC706/cVdDZo2N7Ieh5ZB1GjLlKafuAqLQOOChHozAOGDvIejHUL41X39VjsoI/AqJkhN65xPT07Y4jjCN5Q1i+Fm5xZeM/nEumnaPIQ2uFIw3fehtNcwzjg1+IbWC6JxVYAth7w9oRwaqSN2f+zM7jgkePO6tB4GkeHH227yTr38VhgxlihodWaSKTasLLgE6RBBv5UzYN7S3d03QHpAsYv/jz4SS4fh37XoJvWbkLZyAcFZrFYjb82D2xntV8AQfROvWb6nRPXCt4u+RvFabBnC8kTAHrNCC2yx4ru9trr5+andSCuNSdH0JpuqtXowWRIh8ps= gurmeet@g
```
#### Register SSH key at github
 - Go to Settings > SSH and GPG Keys
 - Under SSH keys section > Click on 'New SSH Key' button at top right corner
 - Enter name of the key 'CirclePC'
 - Copy and paste pub key text ssh-rsa AAAAB....RIh8ps= gurmeet@g
 - Click on 'Add SSH Key'
 - New SSH key will apear. SHA256:/Uv/LaozGObWT4y2c+KYSUU5y4wYfirmRVRtY9DxOGA




#### Clone a repository at PC
- Copy the SSH link from Github 
```
$  sudo apt install git 
$  git config --global user.email "gsdhillon@gmail.com"
$  git config --global user.name "Gurmeet Singh"
$  cd ~
$ git clone git@github.com:gsdhillon/Ajaybir.git
Cloning into 'Ajaybir'...
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
$ cd Ajaybir
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

#### Create alias for Add ., Commit -m "-", git push, git status
```
git config --global alias.acp '!f() { git add . && git commit -m "-" && git push && git status; }; f'
```
##### Test alias acp  
```
$ git acp
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 434 bytes | 434.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:gsdhillon/Ajaybir.git
   c275c03..f58ed92  main -> main
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```
#### To create new repository and push:
```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://gsdhillon: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@github.com/gsdhillon/Chemistry.git
git push -u origin main
```
