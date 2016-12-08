# 1.设计目标 # 
提升Git使用效率

# 2.实现步骤 #
	
	STEP1.从git仓库克隆，使用Git工作流初始化此仓库，自动切换到develop分支
	STEP2.开发人员从develop分支创建feature分支进行特性开发，完成此分支可以自动合并到develop分支并删除当前feature分支（此时可能会发生冲突）
	STEP3.从develop分支创建release版本，可以在此分支上进行bug修复，并按照需求手动merge到develop分支，完成release版本时，会同时推送到master和develop（此时可能发生冲突）
	STEP4.从master上拉取hotfix分支进行bug修复，完成时会推送到master和develop并删除当前hotfix分支（此时可能发生冲突）
	注意：每个仓库都可以创建hotfix分支与release分支
	
# 3.Commiter注意点 #
	
	从release上传到master，可以通过sourceTree查看曾经上传的历史
	
# 4.reference #
	
	https://my.oschina.net/jiangchike/blog/380070
	