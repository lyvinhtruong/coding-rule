# Working with GIT

First, let view the Git branches map as below picture:

![Github Operation Workflow](https://github.com/truonglv-eva/coding-rule/blob/master/images/git-work-flow.png?raw=true)


### 1. Coding:
* `develop` is the common branch for developer to get the latest source code when coding
* Developer must checkout a new branch (feature branch) from branch `develop` when starting a new task, name of branch should be similarly meaning with task name

  For example:
 ```
 git checkout develop
 git fetch origin
 git pull origin develop
 git checkout -b contact-page
 ```


### 2. Committing:
* The first, you need to add something to commit:
 ```
 git add example.php
 ```

* Then, let's commit.
 ```
 git commit -m "typing your message here"
 ```

* Pushing is the most important operation in committing phase, before pushing your code, you must `rebase` your source code first, in some case you may fix conflicts during rebasing
  
  Rebasing will be doing like below:
  
 ```
 git checkout develop
 git fetch origin
 git pull origin develop
 git checkout contact-page
 git rebase -i develop
 ```

  Then let `push` it
  
  ```
  git push origin contact-page
  ```


### 3. Pull Request:
* After pushing your feature branch, create a Pull Request on Github, the name of Pull Request should be same meaning of your task. Example: _**Make contact page**_
* You should write a description or explain about your code in Pull Request
* You must copy and paste the URL of the related issue into the comment section of your Pull Request like this: _**Resolve issue [Issue_URL]**_


### 4. Review code:
* When reviewing code, you must check for [Coding Styles](https://github.com/truonglv-eva/coding-rule/blob/master/wordpress-coding-standards.md) on Pull Request
* You should also give your idea by comment in the Pull Request (Ex: Report bugs (required), remind or suggest a better solution (optional),...)


### 5. Testing:
* Tester will do this on the test server
* Tester will checkout (and pull) code from feature branch of current task (to be reviewed) on test server

  For example
  ```
  git fetch origin
  git checkout contact-page
  git pull origin contact-page
  ```

* After finish or pending testing phase, tester must checkout back to `develop` branch
 ```
 git checkout develop
 ```

* Tester will reports bugs by comment on issue


### 6. Release:
* Publisher will merge code from all (released) Pull Requests (merge feature branch into `develop` branch), then delete feature branch on Github also
* Then, publisher will merge `develop` branch into `master` branch
* Next, checkout a new tag for releasing on Github
  
  ```
  git tag -a v1.4 -m "my version 1.4"
  ```

* Then, push the new tags into Github:

  ```
  git push origin --tags
  ```

* Finally, publisher will release latest source from `master` branch to live server


Next:
[Wordpress Coding Standards](https://github.com/truonglv-eva/coding-rule/blob/master/wordpress-coding-standards.md)
