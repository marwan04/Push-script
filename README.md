# Git Interactive Add Script

This repository contains a Bash script that helps you **interactively select which changed files to stage and commit** in a Git repository.

Instead of manually running `git add` for each file, this script presents you with a menu where you can choose specific files, add all remaining files, or quit without making changes.

---

## Features

✅ Detects if the current folder is a Git repository  
✅ Shows unstaged changes in a numbered list  
✅ Allows you to:
- Add individual files one by one
- Add all remaining changes at once
- Finish selection whenever you’re ready
- Quit safely without committing anything

✅ Prompts for a commit message  
✅ Runs `git add`, `git commit`, and `git push`

---

## Usage

1. Save the script (e.g. as `git-interactive-add.sh`)  
2. Make it executable:

    ```bash
    chmod +x git-interactive-add.sh
    ```

3. Run it from the root of your Git repository:

    ```bash
    ./pusher.sh
    ```

---

## Example

When you run the script, you’ll see something like this:

Select a file to add:
1) src/main.py
2) README.md
3) tests/test_main.py
a) Add all remaining
d) Done selecting files
q) Quit
Choice:


- Enter a number to stage that file  
- Enter `a` to stage everything left  
- Enter `d` to finish your selection and proceed to commit  
- Enter `q` to quit without making changes  

Then you’ll be prompted:

Enter commit message:

Type your commit message, and the script will:

- Stage the selected files
- Create the commit
- Push it to your current branch

---

## Notes

- The script checks if you’re inside a Git repository and exits safely if not.
- Empty commit messages are not allowed.
- This script uses `git status --porcelain` to detect changes.

Feel free to modify it for your workflow!
