##1.设计目标##
提升Git使用效率

##2.实现步骤(C版本开始时)##
**STEP1.从git仓库克隆，使用Git工作流初始化此仓库，自动切换到develop分支**	
	
	角色：Commiter(monkey)
	频率：1个C版本1次
	
##3.实现步骤(特性开发时)##
**STEP1.开发人员从develop分支创建feature分支进行特性开发，完成此分支可以自动合并到develop分支并删除当前feature分支**
		
	角色：特性负责人
	频率：特性上车时1次
	是否存在合并代码工作量：此时可能会发生冲突，需要各组、集中1天、协同合代码
	
**STEP2.从develop分支创建release版本，可以在此分支上进行bug修复，并按照需求手动merge到develop分支，完成release版本时，会同时推送到master和develop**
		
	角色：Commiter(monkey)
	频率：N个特性上车准备集中交付时1次
	是否存在合并代码工作量：此时可能会发生冲突，需要各组、集中1天、协同合代码
	操作技巧：从release上传到master，Commiter可以通过sourceTree查看曾经上传的历史
	
##4.实现步骤(维护时)##
**STEP1.从master上拉取hotfix分支进行bug修复，完成时会推送到master和develop并删除当前hotfix分支**
	
	角色：Commiter(monkey)
	频率：每天、主线有问题单、小需求单时
	是否存在合并代码工作量：此时可能会发生冲突，需要各组、集中、协同合代码（此时可能发生冲突）
	操作技巧：从release上传到master，Commiter可以通过sourceTree查看曾经上传的历史
	
##5.对测试的变化##
	
	测试主线版本的作用：保证Hotfix
	测试Release版本的作用：保证新特性

##6.reference##
	
	https://my.oschina.net/jiangchike/blog/380070
	注意：每个仓库都可以创建hotfix分支与release分支
	