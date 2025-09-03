# GitHub 简要使用说明

GitHub 是一个基于 Git 的代码托管平台和协作开发平台。以下是一些基本概念和常用操作：

## 基本概念

*   **仓库 (Repository/Repo):** 项目的存储空间，包含所有项目文件、文件夹、图片、视频、数据集以及修订历史记录。
*   **分支 (Branch):** 仓库的独立版本。默认分支通常是 `main` 或 `master`。开发者可以在不影响主线的情况下在分支上进行开发。
*   **提交 (Commit):** 对仓库中文件所做的更改的快照。每次提交都有一个唯一的 ID 和一条描述更改内容的消息。
*   **拉取请求 (Pull Request/PR):** 提议将一个分支的更改合并到另一个分支（通常是 `main` 分支）。PR 允许团队成员审查代码、讨论更改并最终合并。
*   **克隆 (Clone):** 在本地计算机上创建远程仓库的副本。
*   **推送 (Push):** 将本地提交上传到远程仓库。
*   **拉取 (Pull):** 从远程仓库获取最新更改并将其合并到本地仓库。
*   **合并 (Merge):** 将一个分支的更改整合到另一个分支。

## 常用 Git 命令

**前提：** 你需要在本地安装 Git ([https://git-scm.com/downloads](https://git-scm.com/downloads))。

1.  **配置 Git:**
    ```bash
    git config --global user.name "你的用户名"
    git config --global user.email "你的邮箱地址"
    ```

2.  **创建新仓库或克隆现有仓库:**
    *   **初始化新仓库:** 在项目文件夹中运行 `git init`。
    *   **克隆远程仓库:** `git clone <仓库URL>`

3.  **基本工作流程:**
    *   **查看状态:** `git status` (查看哪些文件被修改、暂存)
    *   **添加文件到暂存区:**
        *   添加特定文件: `git add <文件名>`
        *   添加所有更改: `git add .`
    *   **提交更改:** `git commit -m "你的提交信息"` (描述你做了什么更改)
    *   **推送更改到远程仓库:** `git push origin <分支名>` (例如: `git push origin main`)
    *   **拉取远程仓库的更改:** `git pull origin <分支名>` (例如: `git pull origin main`)

4.  **分支管理:**
    *   **查看所有分支:** `git branch`
    *   **创建新分支:** `git branch <新分支名>`
    *   **切换到分支:** `git checkout <分支名>` 或 `git switch <分支名>` (较新版本 Git)
    *   **创建并切换到新分支:** `git checkout -b <新分支名>` 或 `git switch -c <新分支名>`
    *   **合并分支:** 先切换到目标分支 (如 `main`)，然后运行 `git merge <要合并的分支名>`
    *   **删除分支:** `git branch -d <分支名>` (注意：通常在合并后删除)

5.  **查看历史:**
    *   **查看提交日志:** `git log`

## GitHub 网页操作

*   **创建仓库:** 点击右上角 "+" -> "New repository"。
*   **创建 Pull Request:** 在你的分支页面，点击 "Compare & pull request"。
*   **代码审查:** 在 Pull Request 页面查看文件更改，添加评论。
*   **合并 Pull Request:** 如果审查通过，点击 "Merge pull request"。
*   **Issues:** 用于跟踪任务、增强功能、Bug 或其他项目相关讨论。
*   **Actions:** 用于自动化构建、测试和部署流程 (CI/CD)。
*   **Fork:** 创建一个仓库的个人副本，允许你在不影响原始项目的情况下自由实验。

这是一个非常基础的指南。GitHub 和 Git 功能强大，还有很多高级用法等待探索。建议查阅官方文档 ([https://docs.github.com/](https://docs.github.com/)) 获取更详细的信息。
