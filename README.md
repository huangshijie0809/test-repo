# 我的第一个 GitHub 仓库

# =======================================================
# 1. 系统已有 OpenSSH 的检查与启用
where ssh  

# 安装 OpenSSH 客户端（管理员权限） (忽略)
Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0  

# 如果你还没生成 SSH 密钥，可以运行：
ssh-keygen -t ed25519 -C "your_email@example.com"  

# 然后将 C:\Users\Administrator\.ssh\id_ed25519.pub 的内容添加到 GitHub/GitLab。 （复制公钥（粘贴到 GitHub Settings → SSH and GPG keys））
cat ~/.ssh/id_ed25519.pub  
或  
cat /c/Users/Administrator/.ssh/id_ed25519.pub  

# 验证 SSH 连接
ssh -T git@github.com  

# =======================================================
# 1. 创建并进入项目目录（可选）
mkdir my-first-repo && cd my-first-repo  

# 2. 创建README.md文件
echo "# 我的第一个 GitHub 仓库" > README.md  

# 3. 设置git全局配置（只需设置一次）
git config --global user.name "你的GitHub用户名"  
git config --global user.email "你的GitHub注册邮箱"  

# 4. 初始化本地仓库
git init  

# 5. 提交到本地仓库
git add README.md  
git commit -m "初始化项目"  

# 6. 重命名分支为main（GitHub默认分支）  
git branch -M main  

# 7. 关联远程仓库（注意替换yourname/your-repo）   
git remote add origin git@github.com:yourname/your-repo.git  

# 8. 首次推送
git push -u origin main  

# 后续推送只需：
git push  





# =======================

# 后续获取更新的内容（下次 git pull 前建议先提交或暂存：）
git stash        #临时保存未提交的修改  
git pull         #拉取更新  
git stash pop    #恢复修改（如有冲突需手动解决）  


# 运行 git log 查看详细的提交历史
git log --oneline  # 简洁版提交记录（只显示哈希和提交信息）  
git log # 完整历史记录  
# 想撤销这次更新？（回退到 git pull 前的状态）
git reset --hard cbe7b28  # 用你的旧提交哈希替换  

#  其他获取哈希值的方式
git reflog #即使回退了代码，仍可通过此命令找回“丢失”的提交  

# 运行 git status 确认工作区是否干净。(如果需要推送本地新提交到 GitHub)
git push origin main  


# =======================
idea 打开 这是我第一次使用 Git + GitHub。



