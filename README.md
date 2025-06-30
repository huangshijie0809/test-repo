# 我的第一个 GitHub 仓库


echo "# 我的第一个 GitHub 仓库" > README.md
git add README.md

git config --global user.name "名称"
git config --global user.email "邮箱"

//提交
git commit -m "初始化项目"
git branch -M main

//把本地仓库和你 GitHub 上的仓库关联起来（设置远程地址（只需一次））
git remote add origin git@github.com:gitHub用户名/仓库名.git
//推送到 GitHub
git push -u origin main
