
# Short Introduction to GitHub

This is the introduction of basic operations of [git bash](https://gitforwindows.org/).
There are better resouces available from [git](https://github.com/git-for-windows/git/tree/master/Documentation) and [Pro Git book](https://git-scm.com/book/en/v2)

## Basic Stuff

* Create a local folder
* Go to that folder from git

     ![](images/intro1.png)
* Initialize git in your local folder


```python
    $ git init
```

* Set remote so you can pull new objects from the repository
    The syntax is `git remote add [shortname] [url] `
    


```python
    $ git remote add origin https://github.com/stomioka/sdtm_mapper.git
```

    or if you are updating it<br>


```python
    $ git remote set-url origin https://github.com/stomioka/sdtm_mapper.git 
```

* You can confirm your remote repository by<br>
    


```python
    $ git remote -v    
```

   ![](images/intro2.png)
 
* Get objects from master repository<br>
    
     You can clone it or pull.   
     
     If you are cloning, you don't need to use `git init`
    


```python
    $ git clone https://github.com/stomioka/sdtm_mapper
    
    $  git pull origin master
```

   ![](images/intro3.png)
     
* You can edit, make updates to the objects locally

* To see any updated objects

    


```python
    $ git status   
```

  ![](images/intro4.png)
     
     In this example, word2vec_tfidf.ipynb has been updated
     
* Add files to be committed. You can specify the folder to add, then all files in the folder will be added.

    


```python
    $ git add word2vec_tfidf.ipynb    
```

   ![](images/intro5.png)
    
* Commit. Git stores a commit object along with author's name and email address

    


```python
    $ git commit -m "add"    
```

  ![](images/intro6.png)
    
* Push to the repository (in this case master)


```python
    $ git push origin master
```

   ![](images/intro7.png)
    
* If you need to **delete** a file,


```python
    $ git rm your_file.txt

    $ git commit -m 'remove'
    
    $ git push origin master
```



Next topic: [Branching](branching.ipynb)
