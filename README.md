# temp nnnn
# ------------------ Lab 1: Setting Up and Basic Commands ------------------
mkdir project1
cd project1
git init
touch file1.txt
git add file1.txt
git commit -m "Initial commit: added file1.txt"
cd ..

# ------------------ Lab 2: Creating and Managing Branches ------------------
mkdir project2
cd project2
git init
touch main.txt
git add main.txt
git commit -m "Initial commit"
git branch feature-branch
git checkout master
git merge feature-branch
cd ..

# ------------------ Lab 3: Stashing Changes and Switching Branches ------------------
mkdir project3
cd project3
git init
touch test.txt
git add test.txt
git commit -m "Initial commit"
echo "New changes" >> test.txt
git stash
git branch new-branch
git checkout new-branch
git stash apply
cd ..

# ------------------ Lab 4: Clone a Remote Repository ------------------
mkdir project4
cd project4
git clone https://github.com/user/repository.git
cd ..

# ------------------ Lab 5: Fetch and Rebase Local Branch ------------------
mkdir project5
cd project5
git init
git remote add origin https://github.com/user/repository.git
git fetch origin
git checkout master
git rebase origin/master
cd ..????////
mkdir project5
cd project5
git init
git remote add origin https://<GITHUB_USERNAME>:<TOKEN>@github.com/<USERNAME>/<REPOSITORY>.git
git fetch origin
git checkout master
git rebase origin/master


# ------------------ Lab 6: Merge a Branch with Custom Commit Message ------------------
mkdir project6
cd project6
git init
touch app.txt
git add app.txt
git commit -m "Initial commit"
git branch feature-branch
git checkout master
git merge feature-branch -m "Merged feature-branch into master with custom message"
cd ..

 7->mkdir project7
cd project7
git init
touch file.txt
git add file.txt
git commit -m "Initial commit"
git tag v1.0


8->
mkdir project8
cd project8
git init

# Initial commit on main/master
touch file.txt
git add file.txt
git commit -m "Initial commit"

# Create source branch and switch to it
git branch source-branch
git checkout source-branch

# Commit 1 on source-branch
echo "Change 1" >> file.txt
git add file.txt
git commit -m "Commit 1 on source-branch"

# Commit 2 on source-branch
echo "Change 2" >> file.txt
git add file.txt
git commit -m "Commit 2 on source-branch"

# Commit 3 on source-branch
echo "Change 3" >> file.txt
git add file.txt
git commit -m "Commit 3 on source-branch"

# View commit hashes
git log --oneline

# Switch back to main/master
git checkout master

# Cherry-pick a range of commits from source-branch
git cherry-pick <commit1>^..<commit3>


