### Wedding Scenario
---

- Imagine you're at a wedding. The couple is on the stage, and guests come up to take pictures with them. The photographer takes the picture, which then becomes part of the wedding album.
    1. **Untracked Guests:** Guests who have arrived but have not yet come to the stage for a photo.
    2. **Staging Area:** Guests who are on the stage, ready for their photo to be taken.
    3. **Commit:** The act of the photographer taking the picture.
    4. **Remote Repository:** The online storage where the wedding album is saved.
    5. **Stashing:** Temporarily sending guests backstage, saying, "Whenever I need you for the photo, I’ll call you."

### Initialize a Local Repository and Upload to GitHub

---

1. **Initialize Git in the Local Folder**
    - **Wedding Scenario:** Setting up the stage for the wedding ceremony.
    
    ```bash
    git init
    ```
    
2. **Add All Files to Staging Area**
    - **Wedding Scenario:** Guests come to the stage and stand with the couple, ready for the photo.
    
    ```bash
    git add .
    ```
    
3. **Commit the Staged Files**
    - **Wedding Scenario:** The photographer takes the picture.
    
    ```bash
    git commit -m "commit message"
    ```
    
4. **Rename the Default Branch to `main`**
    - **Wedding Scenario:** Naming the wedding album.
    
    ```bash
    git branch -M main
    ```
    
5. **Add Remote Repository**
    - **Wedding Scenario:** Deciding where to store the wedding album.
    
    ```bash
    git remote add origin <link>
    ```
    
6. **Push Local Repository to GitHub**
    - **Wedding Scenario:** Uploading the wedding album to an online storage service.
    
    ```bash
    git push -u origin main
    ```
    

### Removing a File from Git

---

1. **Remove a File from Git and Local System**
    - **Wedding Scenario:** Removing a guest from the photo and the wedding venue.
    
    ```bash
    rm -rf <filename>
    ```
    
2. **Remove a File from Git but Keep it Locally**
    - **Wedding Scenario:** Removing a guest from the photo but letting them stay at the venue.
    
    ```bash
    git rm --cached <filename>
    ```
    

### Undo Mistakenly Staged Files

---

1. **Unstage a File Before Commit**
    - **Wedding Scenario:** Guest steps away from the stage before the photo is taken.
    - If you mistakenly staged a file (using `git add <filename>`) and want to unstage it before committing.
    
    ```bash
    git restore --staged <filename>
    ```
    

### Undo Mistakenly Committed Files

---

1. **Reset to a Previous Commit**
    - **Wedding Scenario:** Going back to a previous point in the wedding album, undoing the addition of some guests.
    - If you mistakenly committed a file and want to undo the commit.
    
    ```bash
    git reset <hash_id>
    ```
    

### Discard Changes of Modified Files

---

1. **Check the Status of Modified Files**
    - **Wedding Scenario:** Checking to see which guests have already taken photos but want to change their outfits (i.e., modified files).
    
    ```bash
    git status
    ```
    
2. **Discard Changes in a Specific Modified File**
    - **Wedding Scenario:** The photographer tells a guest they can go back and change their outfit, and the original photo is kept.
    
    ```bash
    git restore <filename>
    ```
    
3. **Discard Changes in All Modified Files**
    - **Wedding Scenario:** The photographer allows all guests to change their outfits, returning to the original look for everyone.
    
    ```bash
    git restore .
    ```
    

### Stashing Changes

---

1. **Stash Changes**
    - **Wedding Scenario:** The photographer tells the guests to go backstage, saying, "Whenever I need you for the photo, I’ll call you." This temporarily removes them from the stage but keeps their place reserved.
    
    ```bash
    git stash
    ```
    
2. **Apply Stashed Changes**
    - **Wedding Scenario:** The photographer calls the guests back to the stage for the photo, bringing them back from backstage.
    
    ```bash
    git stash pop
    ```
    
3. **Clear Stashed Changes**
    - **Wedding Scenario:** The photographer decides they don’t need the guests anymore and sends them home, clearing the reservation for the photo
    
    ```bash
    git stash clear
    ```
    

### General Git Workflow

---

1. **Check Status (Untracked Files)**
    - **Wedding Scenario:** Checking to see which guests are untracked, meaning they haven’t had their photo taken yet (i.e., they are not staged or committed).
    
    ```bash
    git status
    ```
    
2. **Fetch Updates from Remote Repository**
    - **Wedding Scenario:** Checking for new guests who arrived at the wedding.
    
    ```bash
    git fetch origin
    ```
    
3. **Switch to Your Branch**
    - **Wedding Scenario:** Moving to your specific spot in the wedding to handle your tasks.
    
    ```bash
    git checkout mitesh_development
    ```
    
4. **Merge Changes from Another Branch**
    - **Wedding Scenario:** Combining photos from another camera into the main wedding album.
    
    ```bash
    git merge origin/development
    ```
    
5. **Commit Merge if Conflicts Resolved Manually**
    - **Wedding Scenario:** Finalizing the combined wedding album after resolving any issues with the photos.
    
    ```bash
    git commit -m "Merge branch 'development' into mitesh_development"
    ```
    

### Merging remote branch to yours branch

---

### Steps to Pull Changes After Merging

1. **Ensure You Are on Your Branch**
    - Before pulling, confirm you are still on your `mitesh_development` branch:
    
    ```bash
    git checkout mitesh_development
    ```
    
2. **Fetch Updates from the Remote Repository**
    - It's a good practice to fetch the latest changes from the remote to ensure you're aware of any new commits:
    
    ```bash
    git fetch origin
    ```
    
3. **Merge the changes from the development branch into your branch**

    
    ```jsx
    git merge origin/development
    ```
    
4. **Pull Changes from the Remote Branch**
    - To pull the changes from the remote `development` branch (or another relevant branch, depending on your workflow), you can run:
    
    ```bash
    git pull origin development
    ```
    
5. Push your commits to the remote mitesh_development branch

---



# Example Scenario for better understanding Merging remote branch to yours

---

I am working in Live project with team of Frontend and backend developer. I am working in frontend. We are tracking our project using Git. And 'development' is our main branch. All developers have created their own branch. My branch name in git 'mitesh_developement' where I push my code. Now, I am updating my branch using GitHub Desktop software in my laptop.

Step 1:  Fetch Origin
Step 2: Choose a branch to merge into `mitesh_developement`
Step 3: Select branch to merge into `mitesh_developement`
Step 4: Create a merge commit

But if I want to do the same thing in GitBash CLI then how can I do

---

1. **Fetch Origin**:
    
    ```bash
    git fetch origin
    ```
    
2. **Choose a branch to merge into `mitesh_development`**:
    
    ```bash
    git checkout mitesh_development
    ```
    
3. **Select branch to merge into `mitesh_development`** (replace `branch_name` with the name of the branch you want to merge):
    
    ```bash
    git merge branch_name
    ```
    
4. **Create a merge commit** (this will automatically happen if there are no conflicts; if there are conflicts, resolve them first and then commit):
    
    ```bash
    git commit
    ```
    

To summarize the steps in one sequence:

```bash
git fetch origin
git checkout mitesh_development
git merge branch_name

```

If there are merge conflicts, you need to resolve them manually. After resolving conflicts, you can finalize the merge with:

```bash
git add .
git commit
```

This process mirrors what you're doing in GitHub Desktop but through the command line.
