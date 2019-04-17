
分支概览
---
- 基本分支
 - 主干分支 (master) `锁定，只允许Pull Request合并`
 - Develop分支 (Develop) `开发分支，日常开发PUSH分支`
- 类分支
 - Release类分支 (release) `锁定, 只允许从master分支独立创建`
 - Hotfix类分支 (Hotfix) `热修复分支,与{Master}始终保持一直`
开发流程
---
- 任务开发
	对应功能开发前先checkout出自己的工作分支，该分支只存在于本地环境开发完成后切换到develop后进行pull & merge然后PUSH到develop分支
	- `git checkout -b dev_xx`
	在本地新建并切换到一个新的开发工作分支 ( `dev_` 开头 个人习惯)
	- `git checkout develop`
	本地dev测试无误后切换到 develop分支
	- `git pull` 
	在develop分支进行pull
	- `git merge dev_xx`
	合并dev_xx到 当前所在分支 (develop)
	- `git push`
	PUSH到远端进行仿真测试
	develop分支仿真测试通过 则在GIT平台发起对Master的合并请求 ( Pull Request )
	责任人对代码进行review，确认无误后通过相应的pull request否则打回重审

- BUG热修 ( Hotfix )
 - 查看线上日志进行相关问题定位
 - 从当前master分支 生成 新的工作分支
`git checkout -b bug_xx` (！重要！创建新分支前务必确认自己当前所在是`master`分支 : `git branch`)
 - 合并并推送到 develop 分支
 - ！！重要！！在develop分支测试无误后 将本地`bug_xx`分支推送到线上并生成新分支然后发起对`master`分支的Pull Request
 - 所有测试无误后删除本地和线上`bug_xx`分支 (或留档待查)
 - 所有热修分支绝对不能二次使用
- 机动修复
 恶意操作无法操作`master`分支，如果`develop`分支被恶意篡改或删除，则删除整个`develop`分支并删除线上`develop`分支然后从`master`分支重新checkout名为`develop`分支即可
