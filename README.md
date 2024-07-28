echo '.env' >> .gitignore
git rm -r --cached .env
git add .gitignore
git commit -m 'untracking .env'
git push origin master


delete all commits
git filter-branch --index-filter "git rm -rf --cached --ignore-unmatch .env" HEAD
git push --force
