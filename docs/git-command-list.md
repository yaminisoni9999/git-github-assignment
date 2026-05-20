# List of Commands

## Question 1

```bash
git --version

git config --global user.name "Yamini Soni"
git config --global user.email "yaminisoni9999@gmail.com"
git config --list

cd D:/hero-vired/assignments/git-github
mkdir git-github-assignment
cd git-github-assignment
mkdir docs
mkdir src
mkdir src/git-github-assignment
mkdir assets
mkdir assets/images
touch README.md
touch requirements.txt
touch docs/git-command-list.md
touch src/git-github-assignment/app.py
find . -print

git init
# rm -rf .git
echo "print('Hello, This is a python file for github assignment.')" > src/git-github-assignment/app.py
git status
git add src/git-github-assignment/app.py
# git add .
git commit -m "Initial commit: add code in app.py"

git remote add origin https://github.com/yaminisoni9999/git-github-assignment.git
git remote -v

git branch -M main
git push -u origin main
#git push
```

## Question 2

```bash
echo "print('Added a new functionality.')" > src/git-github-assignment/app.py
git status

git diff rc/git-github-assignment/app.py
git add -p
git commit -m "updated app.py file => added new functionality"

echo "print('This is a new change.')" > src/git-github-assignment/app.py
git add .
git commit -m "updated app.py file => new change"

git log

git log --oneline
```

## Question 3

```bash
git branch feature-update
git checkout feature-update
echo "print('This is a new change from feature branch')" > src/git-github-assignment/app.py
git add .
git commit -m "updated app.py file => add new feature from feature branch"
git push -u origin feature-update

git checkout main
git merge feature-update
git push origin main
git log --oneline

git log --oneline --graph --all

git branch -d feature-update
git branch
git branch dummy-branch
git branch -D dummy-branch
git branch
git push origin --delete feature-update
```

## Question 4

```bash
echo "print('work in progress')" > src/git-github-assignment/app.py
git stash -u
git stash list
git stash apply
git add .
git commit -m "updated app.py file and applied stashed changes"
git log --oneline

echo "print('incorrect code')" > src/git-github-assignment/app.py
git add src/git-github-assignment/app.py
git commit -m "updated app.py file => incorrect code"
git log --oneline -n 5
git reset --soft HEAD~1
git log --oneline

echo "print('correct code')" > src/git-github-assignment/app.py
git add src/git-github-assignment/app.py
git commit -m "updated app.py file => correct code"
git log --oneline -n 5
git revert HEAD
git log --oneline
```