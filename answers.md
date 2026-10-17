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
# 6. Why did we commit A+B separately from C? When would you want to split commits this way?
# Answer: we commit A+B separately from C because A+B might have similar values , whereas C might be totally different from A,B. which means that committing A+B will give zero conflicts and commiting them with C might give many conflicts.

# 6. What would happen if you made a local commit first WITHOUT pulling? What command helps you check?
# Answer: if we make a local commit first without pulling then our local branch and remote github branch will not match because each have a commit which the other does not have. the git push command will help us check, because it will give a error, failing to push.


# 9. In answers.md : Did this merge create a merge commit or was it a fast-forward? How
# can you tell?

# it created a fast-forward because it gave us no error message of commit first and in the result fast-forward is also written  