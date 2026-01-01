md .minecraft
cd .minecraft

rmdir .git /s /q
git init
git remote add origin https://github.com/kartjom/mc-mods.git
git pull origin master

cd ..

@echo off
echo cd .minecraft > Update.bat
echo git reset --hard origin/master >> Update.bat
echo git fetch >> Update.bat
echo git pull origin master --rebase >> Update.bat

Update.bat
