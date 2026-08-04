# Level 0 → 1

## Challenge
We are given the task of finding the password of user bandit1, and they mention the password is located in a readme file. Once we locate the password, we need to ssh into bandit1.

## Approach
- We take a very straightforward approach first we list all the files in the current directory with `ls`
- Once we find our readme, we just need to `cat` it and copy the password
- Then you just need to ssh into `bandit1@bandit.labs.overthewire.org` with port 2220

## Commands Used
- `ls` to list all the files
- `cat` to display the file
- `ssh` to connect to the next level

## Notes
Pretty easy first level, just getting used to ssh and basic navigation. One thing that tripped me up you can't ssh into the next level from inside your current session (it blocks localhost connections), you gotta run the ssh command from your own terminal.
