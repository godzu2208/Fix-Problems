### GitHub-Problems
# How to Push an Existing Project to GitHub

git init \
git add .\
git commit -m "commit files"\
git remote add origin https://github.com/godzu2208/web-react.git  \
git push -u origin master 

#OR
git init \
git add -A \
git commit -m 'Added my project' \
git remote add origin git@github.com:sammy/my-new-project.git \
git push -u -f origin master \


# How to solve this problem of "! [rejected] master -> master (fetch first)"
#First Do this ...
git fetch origin master
git merge  master

#Then, do this ...

git fetch origin master:tmp
git rebase tmp
git push origin HEAD:master
git branch -D tmp

#Now everything works well.
