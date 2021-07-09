Git naming convention for this project
===================================

How to name branch, commit and push code and working flow in the project and more.


## Some links for more in depth learning
### Hands on / interactive learning
* [Learn Version Control with Git](https://www.git-tower.com/learn/ebook) A website for learning Git. Appears to cost money but has a free html book.
* [Git Immersion](http://gitimmersion.com/lab_01.html) A website with tutorial materials you download and follow along with.
* [Try Git](http://try.github.io/levels/1/challenges/1) A 15 minute interactive tutorial to learn the basics. 
* [Git-it](http://nodeschool.io/#git-it) Interactive software you run from the Terminal (requires installing node.js and nmp).

Setting up
------------
Assume the project in a folder named "TLC"

Cloning an existing repository

- Determine your SSH clone url. On Github it's probably something like ***git@github.com:USERNAME/PROJECT.git***. Should be on the project's page somewhere.

		cd ~/Desktop
		git clone {{the link you just copied}} Project

- This creates a directory named "Project", clones the repository there and adds a remote named "origin" back to the source.

		cd Project
		git checkout develop

- If that last command fails

		git checkout -b develop


Updating/The Development Cycle
------------
You now have a git repository, likely with two branches: master and develop. Now bake these laws into your mind and process:

####You will never commit to ***master*** directly.
####You will never commit to ***development*** directly.

Instead, you will create ***feature branches*** on your machine that exist for the purpose of solving singular issues. You will always base your features off the develop branch.

Branch naming convention of this project: based on **Trello** cards
------------

For example, if the card name is DEV-32

If branch feature/DEV-32 has already existed:
    git checkout feature/DEV-32

If not existed:
		git checkout -b my-feature-branch


Make changes.

	  git add .
	  git commit -am "I have made some changes."


After a member commits the code, the team leader will review the code and then merge it to development branch. After the merge, other members need to pull the changes by:
    git pull origin development
