### GitHub-Problems
# How to Push an Existing Project to GitHub

git init \
git add .\
git commit -m "commit files"\
git remote add origin https://github.com/godzu2208/web-react.git  \
git push -u origin master 

# Another Way
git init \
git add -A \
git commit -m 'Added my project' \
git remote add origin git@github.com:sammy/my-new-project.git \
git push -u -f origin master \


# How to solve this problem of "! [rejected] master -> master (fetch first)"
# First Do this ...
git fetch origin master\
git merge  master

# Then, do this ...

git fetch origin master:tmp\
git rebase tmp\
git push origin HEAD:master\
git branch -D tmp

#Now everything works well.

# How to fix mysql shutdown unexpectedly in xampp while apache working
# Just follow these steps and its done.
    - Rename the folder C:\xampp\mysql\data to C:\xampp\mysql\data_old (you can use any name)
    - Create a new folder C:\xampp\mysql\data
    - Copy the content that resides in C:\xampp\mysql\backup to the new C:\xampp\mysql\data folder
    - Copy all your database folders that are in C:\xampp\mysql\data_old to C:\xampp\mysql\data (skip the mysql, performance_schema, and phpmyadmin folders from C:\xampp\mysql\data_old)
    - Finally copy the ibdata1 file from C:\xampp\mysql\data_old and replace it inside C:\xampp\mysql\data folder
    - Now Start MySQL from XAMPP control panel
