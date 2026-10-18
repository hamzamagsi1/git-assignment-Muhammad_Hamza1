# Git Assignment — Answers
# Part 1 — Concepts & Theory

# Q1. Terminal basics
# Q.  What is a terminal? How is it different from clicking through folders in a file explorer?
# Answer
# a terminal is a way to talk to your computer, you write commands in texts and the computer 
# runs them, it is different from a file explorer in such a way that you use graphical interface to navigate the file explorer whereas in terminal you type commands to navigate and create files and folders.

# Q. Write the terminal command to: (a) list all files including hidden ones, (b) create a
# folder called project , (c) move into that folder
# Answer: PS C:\Users\USER\git-assignment-Muhammad_Hamza1> ls
# PS C:\Users\USER\git-assignment-Muhammad_Hamza1> mkdir project
# PS C:\Users\USER\git-assignment-Muhammad_Hamza1> cd project

# Q. What does the cd .. command do? What about cd ~ ?
# the cd .. takes you up one level
# the cd ~ it takes you back to your user home directory

# Q2. Version control concepts
# 4. Explain what version control is in your own words. Give one real-world analogy (not
# Google Docs — pick your own).
# Answer: version control is a system which records all changes made to files over time. You can use it to go back to a version where the code you were working on was correct. It also help when you are collaborating with people and working on same file. Real world example would be like a saved story line game progress. Where when you reach a level, your progress is saved and you can go back to previous saved game files if you are unable to complete boss level.

# Q.5. What is the difference between Git and GitHub? Can you use Git without GitHub?
# Answer: Git is a software tool installed locally on your pc, it is used to manage, create and work on files. It handles local commits, branching, merging locally and history tracking offline on your machine.
# Github is a cloud based hosting service which is built on top of git. It is used to store repostories remotely and has features like pull requests, issue tracking and team collaboration tools.
# Yes, we can use git locally to manage our project without ever touching github.

# Q.6. Name three features GitHub provides that Git alone does not.
# Answer: the features are cloud remote hosting, pull requests and issue tracking

# 7. What is a repository? What is the difference between a local repository and a remote
# repository?
# Answer: A reporsitory is a storage space which contains a project's files, folders and complete history of commits made in timeline.
# the difference is that in local repository the files and folders are stored offline and we can create, edit, commit and branch offline. Whereas online repository helps us work in team collaboration on same project remotely online.

# Q3. Git internals 
# 8. Explain what HEAD means in Git. What happens to HEAD when you switch branches?
# ANSWER: HEAD tracks where you are currently working in a repository.
# When we switch branches, HEAD detaches from its current location, and attaches itself to the newly mentioned branch. It also updates the timeline along the way.

# 9. What is a .gitignore file? Write a .gitignore that ignores: all .log files, a folder
# called node_modules/ , and any file ending in .env
# Answer: .gitignore tells the system which file and folfiles to not track, it is placed in root directory of the repository.
# *.log
# node_modules/
# .env 

# Exercise 2.2 — The staging area (8 marks)

# 6. Q. Why did we commit A+B separately from C? When would you want to split commits this way?
# Answer: we commit A+B separately from C because A+B might have similar values , whereas C might be totally different from A,B. which means that committing A+B will give zero conflicts and commiting them with C might give many conflicts.

# 2.3
# 6. Q. What would happen if you made a local commit first WITHOUT pulling? What command helps you check?
# Answer: if we make a local commit first without pulling then our local branch and remote github branch will not  # match because each have a commit which the other does not have. the git push command will help us check, because # it will give a error, failing to push.

## Part 3 Questions — Branching & Merging Lab
# 3.1
# 9. Q. Did this merge create a merge commit or was it a fast-forward? How
# can you tell?
# Answer: it created a fast-forward because it gave us no error message of commit first and in the result fast-forward is also written  

# 3.2
# Q.Why did this conflict happen? (Reference the rule: same file, same line)
## Answer: the answer to this question is that this conflict happened because i edited the same two files and only changed one exact line in one specific position in both of them. When i tried to merge them, they were overlapping so git halted the merge. 

# Q.Would there have been a conflict if the two branches edited different lines of
# team.txt ?
# Answer: No, there would not have been any conflict because in that scenario, Git automatically merges the files. # And as Git tracked changes at line level, they would not have overlapped at merging, so git would have observed itself and merged them without human input.

# Q. Would there have been a conflict if one branch edited team.txt and the other
# edited about.md ?
# Answer : No there will no conflict because the team lead told us that if one person is working on one file, and another on other file, then when merging them, git will automatically merge them without any conflict.

# Part 4 — GitHubWorkflow Challenge

# Q.What is the purpose of a pull request? Why not just merge directly?
# Answer: the purpose of pull request is to review the code before merging it, it is a formal and structured way to request to merge. If the code contains erros, we can fix it before merging rather than merging directly and disrupting the whole task.

# Q.Name two things a reviewer should check in a pull request.
# Answer: the reviewver should check wether the code matches their already set rules(format, syntax etc). The person should also check if there are any security vulnerabilitues such as exposed API keys.

# Q.What is the difference between a merge commit and a fast-forward merge?
# Answer: the difference between both is that merge commit is used when there are changes between branches and both have new commits, whereas in fast-forward merge the target main branch has no new commits since the creation of feature branch.

# Part 5 — Merge Conflict Scenarios (10 marks)
# No coding here — read each scenario and write your answers in answers.md . 2 marks per question.

# Scenario A. Ahmed creates a branch and changes line 10 of index.html . Sara creates a
# different branch and changes line 1 of the same index.html . Both merge into main . Will
# there be a conflict? Why or why not?
# Answer: because Ahmed and Sara made changes in different lines of the same file, there will be no conflict
# and git will not require human input, it will automatically merge them. Git gives error when same lines overlap and in this case lines are different, line 1 and line 10.

# Scenario B. Ali edits style.css on his branch. Fatima edits app.js on her branch. Both
# merge into main . Will there be a conflict? Why or why not?
# Answer: git tracks and merges changes on a file to file basis, which means that if two separate files on separate branches have changes , then at time of merge git will automatically merge them and there will be no issue.

# Scenario C. DevA changes line 5 of config.py to DEBUG = True . Dev B changes line 5 of
# config.py to DEBUG = False . Both merge into main . Will there be a conflict? If yes,
# show exactly what the conflict markers would look like in the file.
# Answer: yes, there will be a conflict because git follows the rule, same file same line , and as both files and lines are same, we will get a conflict. the conflict markers will look like
# <<<<<<<HEAD
# DEBUG = True
# ============
# DEBUG = False
# main config.py >>>>>>>

# Scenario D. You run git merge feature/new-ui and see this output:
# Auto-merging index.html
# CONFLICT (content): Merge conflict in index.html
# Automatic merge failed; fix conflicts and then commit the result.
# Write out the exact steps (commands included) you would take to resolve this conflict and finish the merge.
# Answer: first of all we will locate the conflict inside the index.html file, then we will click on the "resolve in merge editor", then it will provide us option which will be choose either file A edit, File B edit, or edit with both merged, or we can type in bottom area our own data. after that save the file, add it, commit it, then push it to github.

# Scenario E. Your teammate says: "I always do git pull before I start working every
# morning." Is this a good practice? Explain why or why not, and what could go wrong if they skip it.
# Answer: doing a git pull before he starts working every morning is a good practice because he is up to date with the latest code, which others have recently edited, he can also see what others have updated so that he doesnt waste hours fixing what was already fixed. One more thing is that git pull every morning might give conflicts but few and manageable, however if a person does git full after a whole week or month, then he will be struck with countless conflicts which will be difficult to resolve.
 