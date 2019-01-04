
# Short Introduction to GitHub

This is the introduction of basic operations of [git bash](https://gitforwindows.org/).
There are better resouces available from [git](https://github.com/git-for-windows/git/tree/master/Documentation) and [Pro Git book](https://git-scm.com/book/en/v2)

## Basic Stuff

## Create a new remote repository (1)
* Create a local folder
* Go to that folder from git

```bash
stomioka@FLNJ23147 MINGW64 /d/git
```

* Initialize git in your local folder

```bash
$ git init
```

* Set remote so you can pull new objects from the repository
    The syntax is `git remote add [shortname] [url] `



```bash
$ git remote add origin https://github.com/stomioka/sdtm_mapper.git
```

or if you are updating it<br>


```bash
$ git remote set-url origin https://github.com/stomioka/sdtm_mapper.git
```

* You can confirm your remote repository by<br>



```bash
$ git remote -v
```

   ![](images/intro2.png)

* Get objects from master repository<br>

     You can pull.



## Create a new remote repository (2)
If you are cloning, you don't need to use `git init`
```bash
$ git clone https://github.com/stomioka/sdtm_mapper

$ git pull origin master
```

![](images/intro3.png)

* You can edit, make updates to the objects locally

---
## Other basic functions

### See any updated objects

```bash
$ git status
```

  ![](images/intro4.png)

In this example, word2vec_tfidf.ipynb has been updated

### Add files to be committed.
You can specify the folder or file(s) to add

```bash
$ git add word2vec_tfidf.ipynb
```

   ![](images/intro5.png)

### Commit
Git stores a commit object along with author's name and email address

```bash
$ git commit -m "add"
```

  ![](images/intro6.png)

### Push to the repository (in this case master)


```bash
$ git push origin master
```

   ![](images/intro7.png)

### Delete a file

```bash
$ git rm your_file.txt

$ git commit -m 'remove'

$ git push origin master
```



Next topic: [Branching](branching.ipynb)
