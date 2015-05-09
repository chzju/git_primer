## git flow

一种双分支结构的，基于提交规则的开发流程

1. `git flow feature finish issue1` 所做的事情：
     <pre>
     - The feature branch 'feature/issue1' was merged into 'develop'
     - Feature branch 'feature/issue1' has been removed
     - You are now on branch 'develop'
     </pre> 

#### develop分支 ####

1. 本地develop:
     * 日常工作的主要分支
1. 远程develop:
     * 用于daily build

#### master分支 ####

1. 永远只提供成品级的代码
     * 通过tag来管理代码的版本
     * 只有新版本发布时，Master才会被用到



#### git-flow参考文档 ####

1. [a-successful-git-branching-model](http://nvie.com/posts/a-successful-git-branching-model/)
1. [中文翻译](http://www.juvenxu.com/2010/11/28/a-successful-git-branching-model/ "中文翻译")
1. [相关工具](https://github.com/nvie/gitflow/)
1. [你为神马不用git-flow呢?](http://www.jeffkit.info/2010/12/860/)