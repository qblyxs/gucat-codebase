# Git命令指南

> 正在完善中

## Git常用命令

| 命令名称                                                     | 作用                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `git config --global user.name 用户名`                       | 设置全局用户名                                               |
| `git config --global user.email 邮箱`                        | 设置全局邮箱                                                 |
| 参数 `--global` 可选项，文件路径用户主目录下 `.gitconfig`    | 使配置全局生效                                               |
| 参数`--local`可选项,文件路径`当前项目/.git/config/`          | 当前项目生效                                                 |
| `git clone 远程仓库地址`<br/>eg:`git clone https://github.com/qblyxs/qblyxs.git` | 将远程仓库的内容克隆到本地                                   |
| `git init`                                                   | 初始化本地库                                                 |
| `git status`                                                 | 查看本地库状态                                               |
| `git add 文件名`<br/>`git add .`                             | 添加到暂存区<br />添加当前全部                               |
| `git rm --cached 文件名`<br/>`git rm --cached *`             | 搁置/移除暂存区文件<br />搁置/移除所有暂存区文件             |
| `git commit -m "日志信息" xxx`<br/>`git commit -m`           | 提交xxx文件到本地库<br />不加文件名表示提交所有              |
| `git commit --amend`                                         | 修改提交日志信息                                             |
| `git reflog`                                                 | 显示所有的操作记录，包括提交，回退的操作                     |
| `git log`                                                    | 显示所有提交过的版本信息，不包括已经被删除的 commit 记录和 reset 的操作 |
| 注意：git reflog 常用于恢复本地的错误操作；<br />场景：我们 `commit` 了一个操作，发现提交的是错误的，于是进行回退，`git reset --hard HEAD^`，就是把工作区的文件也回退还原了，这时候突然发现之前的提前是正确的，想再回退到回退之前的，便去找到之前的版本号进行回退，使用 `git log` 发现之前提交的版本号记录根本不存在了，这时只能使用 `git reflog` |                                                              |
| `git reset --hard 版本号`                                    | 版本穿梭（硬撤销）                                           |
| `git reset --soft 版本号`                                    | 版本穿梭（软撤销）                                           |
| 注意：<br />- 硬撤销：本地代码会直接变更为指定的提交版本，**慎用**！删除工作空间改动代码，撤销 commit，撤销 git add .，注意完成这个操作后，就恢复到了上一次 commit 后的状态<br />- 软撤销：本地代码不会变化，只是 git 转改会恢复为 commit 之前的状态，不删除工作空间改动代码，撤销 commit，不撤销 git add .<br />`git reset --soft HEAD^`：一大用途，撤销 commit，但不撤销 add . |                                                              |
| `git branch 分支名`                                          | 创建分支                                                     |
| `git branch -v`                                              | 查看分支                                                     |
| `git checkout 分支名`                                        | 切换分支                                                     |
| `git merge 分支名`                                           | 把指定的分支合并到当前分支上（可能发生合并冲突，便需要人工解决） |
| `git remote -v`                                              | 查看当前所有远程地址别名                                     |
| `git remote add 别名 远程地址`                               | 为远程地址起别名                                             |
| `git push 别名 分支`                                         | 推送本地分支上的内容到远程仓库                               |
| `git pull 远程库地址别名 远程分支名`                         | 将远程仓库对于分支最新内容拉取下来后与当前本地分支直接合并（可能发生合并冲突，便需要人工解决） |













