# Level 1 → 2

## Challenge
This time the password is stored in a file called `-`, located in the home directory. We just need to find and read it.

## Approach
- First I used `ls` to list everything in the current working directory
- Tried to `cat` the file `-`, but `cat` interpreted it as a special symbol instead of a filename
- Checked the file type of `-` using `file -`
- Tried using `mv` to rename the file, but that didn't help either
- Finally did some digging on Google and understood that I needed to tell `cat` that `-` is not a special character, it's an actual file
- Gave the full path to `cat` instead of just the filename, and that finally gave me the password

## Concept Learned
Filenames that start with a dash (`-`) get misread by commands as flags/options instead of filenames. The fix is to reference the file using a relative (`./-`) or absolute path, so the shell doesn't treat the dash as special.

## Commands Used
- `ls` - list all files
- `pwd` - print current working directory
- `file` - check the file type
- `mv` - attempted to rename the file (didn't end up using this in the final solution)
- `cat` - used with a full/relative path to finally read the file

## Notes
This one took a bit of trial and error. The `-` filename is a classic Linux gotcha since Bash treats it as a stdin/stdout shortcut in a lot of commands. Good lesson in reading command behavior carefully instead of assuming a straightforward `cat filename` will always work.
