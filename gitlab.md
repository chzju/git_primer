## gitlab
1. 刚开始使用git flow的时候经常弄错，所以建议现在自己fork的仓库上使用git flow
2. 项目使用fork-》开发-》merge request的方式开发

### gitlab ci
1. gitlab ci runner可以安装在任何终端上面，通过主动拉取信息来build
2. 每个project被限制只能配置一个build script，估计要好几本版本之后才可以对build脚本进行配置 [reference](https://www.gitlab.com/2013/12/19/gitlab-ci-with-parallel-builds-and-deployments/)