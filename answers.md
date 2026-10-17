# Git Assignment — Answers
# Part 1 — Concepts & Theory (20 marks)
# Complete Part 2 first (create your repo), then come back here. Answer each question in
# your answers.md file. Be concise — 2–3 sentences per question unless stated otherwise.

# Q1. Terminal basics (2 marks each = 6 marks)
# 1. What is a terminal? How is it different from clicking through folders in a file explorer?
# Answer
# a terminal is a way to talk to your computer, you write commands in texts and the computer 
# runs them, it is different from a file explorer in such a way that you use graphical interface to navigate the file explorer whereas you type commands to navigate using terminal.

# Write the terminal command to: (a) list all files including hidden ones, (b) create a
# folder called project , (c) move into that folder
# Answer: PS C:\Users\USER\git-assignment-Muhammad_Hamza1>   


# Exercise 2.2 — The staging area (8 marks)

# 6. Q. Why did we commit A+B separately from C? When would you want to split commits this way?
# Answer: we commit A+B separately from C because A+B might have similar values , whereas C might be totally different from A,B. which means that committing A+B will give zero conflicts and commiting them with C might give many conflicts.

# 6. Q. What would happen if you made a local commit first WITHOUT pulling? What command helps you check?
# Answer: if we make a local commit first without pulling then our local branch and remote github branch will not match because each have a commit which the other does not have. the git push command will help us check, because it will give a error, failing to push.


# 9. Q. Did this merge create a merge commit or was it a fast-forward? How
# can you tell?
# Answer: it created a fast-forward because it gave us no error message of commit first and in the result fast-forward is also written  

## Part 3 Questions — Branching & Merging Lab

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