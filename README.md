# DevOps-LABFILE

# LAB-1 GIT COMMANDS


**This repository contains the practical lab files and exercises related to DevOps, including Git operations and version control demonstrations.**

Cloning the Repository
To begin, clone this repository using the following command:

```bash
git clone https://github.com/SAGAR-SINGH-X-CUBE/DevOps-LABFILE.git
```


![clone command](./fi.png)

**Staging, Committing, and Pushing Changes**
After making changes to the repository (e.g., editing files, creating new ones), use the following commands to stage, commit, and push those changes:

```bash
git add .
git commit -m "figure 1"
git push
```


git add . stages all modified and new files.

git commit -m "figure 1" saves the changes with a commit message.

git push uploads the changes to the remote GitHub repository.



![add,push,commit](./f2.png)

**Checking the Status of Your Working Directory**
To view the current state of your working directory, run:

```bash
 git status 
 ```
![status](./f3.png)


**Viewing Code Differences**
To examine the changes you made before committing, use:

```bash 
git diff
 ```

![diff](./f4.png)







# LAB-2 GIT COMMANDS
*BRANCHING*


Create a file and do 3 commits in it
1st change
```bash
git add .
git commit -m "version1"
```
2nd change
```bash
git add .
git commit -m "version1"
```

3rd change
```bash
git add .
git commit -m "version3"
```



View all commits by using git log

```bash
git log
```

![allcommit](./f5.png)




```bash
git branch featur1
git log
```


![allcommit](./f6.png)

CREATE NEW FILE AND ADD TWO COMMITS
```bash
git add.
git commit -m "feature commit 1"
```
```bash
git add.
git commit -m "feature commit 2"
```



![allcommit](./f7.png)

```bash
git checkout master
git log
```


![allcommit](./f8.png)


#Merging
```bash
git checkout feature1
git log

```

![allcommit](./f9.png)

Do the comit 3 in feature branch
```bash
git add .
git commit -m "feature done"
git log

```

![allcommit](./f10.png)

switching to master branch and perform merging
```bash
git checkout master
git merge feature1 -m "Merging featutre 1"
git log

```

![allcommit](./f11.png)

*RESET*
```bash
git reset --hard a462d13e9a
git log
``` 

*GIT RESET --HARD:Removed the merge commit 13dd279 and deleted all merged changes.*
*GIT RESET --SOFT:Would have removed the merge commit but kept changes staged, allowing you to re-commit easily.*

*REBASE*

```bash
git checkout feature1
git rebase master
git log
``` 

![allcommit](./f12.png)



#GIT SUBMODULE

CREATE THREE REPO IN GITHUB
AND CLONE IT TO YOUR PC
REPO1:MAIN-add index.html file->add->commit->push
REPO2:CSS-add style.css file->add->commit->push
REPO3:JS-add script.js file->add->commit->push


![allcommit](./f13.png)

open integrated terminal of MAIN repo
```bash
git submodule add https://github.com/SAGAR-SINGH-X-CUBE/JS.git css
git submodule add https://github.com/SAGAR-SINGH-X-CUBE/CSS.git css
git add .
git commit -m "submodule added"
git push

```

![allcommit](./f14.png)




#Hosting Submodule
Create a repository with the same name as github username
*SAGAR-SINGH-X-CUBE.github.io*
Go to your repository: SAGAR-SINGH-X-CUBE.github.io
Click on "Settings" → "Pages"
Under "Branch," select main.
Click "Save."

![allcommit](./f16.png)

![allcommit](./f15.png)


#SUBVERSION


>CREATE A REPOSITORY
```bash
sudo mkdir -p /var/svn/repos
sudo svnadmin create /var/svn/repos/myrepo

```
>Confgure SVN Server
```bash
sudo nano /var/svn/repos/myrepo/conf/svnserve.conf

```

![allcommit](./f17.png)

```bash
anon-access = none      # Disable anonymous access
auth-access = write     # Allow authenticated users to write
password-db = passwd    # Use the passwd file for authentication


```
![allcommit](./f18.png)



>SET UP THE USER
```bash
sudo nano /var/svn/repos/myrepo/conf/passwd

```

```bash
alice = alicepassword
bob = bobpassword
```

![allcommit](./f19.png)

>START SVNSERVER

```bash
sudo svnserve -d -r /var/svn/repos

```

>Restart the server
```bash
sudo pkill svnserve
```

```bash
sudo pkill svnserve
```

```bash
cd /path/to/repo/conf/
cd /var/svn/repos/myrepo/conf/
svnserve -d -r /var/svn/repos/

```

>CLIENT SIDE
```bash
svn checkout svn://localhost/myrepo --username alice
cd myrepo

echo "Hello, SVN!" > file.txt
svn add file.txt
svn commit -m "Added file.txt"
svn update
svn status
svn log

```


# FORK

![allcommit](./f20.png)

![allcommit](./f21.png)





# DOCKER

```bash
docker -v

```

```bash
docker pull hello-world

```

```bash
docker images

```

![allcommit](./d1.png)


```bash
docker run hello-world
```

![allcommit](./d2.png)

```bash
docker run -it ubuntu

```

![allcommit](./d3.png)

```bash
docker ps -a

```

![allcommit](./d4.png)

```bash
docker ps -a
docker start youthful_yonath
docker ps
docker stop b8fe5708c23b
docker ps

```

![allcommit](./d5.png)

```bash
docker ps -a
docker start youthful_yonath
docker ps
docker stop b8fe5708c23b
docker ps

```
docker rmi hello-world
docker ps -a
docker rm 33dc638eb2c4
docker rmi hello-world
![allcommit](./d5.png)




# Jenkins

![allcommit](./j1.png)
![allcommit](./j2.png)
![allcommit](./j3.png)
![allcommit](./j4.png)
![allcommit](./j5.png)
![allcommit](./j6.png)
![allcommit](./j7.png)
![allcommit](./j8.png)
![allcommit](./j9.png)
![allcommit](./j10.png)
![allcommit](./j11.png)
![allcommit](./j12.png)
![allcommit](./j13.png)




















