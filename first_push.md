### 远程操作命令
* 从远程复制仓库
     * git clone git@host:repot.git
     * git remote add origin git@host:repot.git # 添加一个远程仓库
* 从远程同步仓库
	* git fetch --all // 从远程拉去所有的修改，但是不合并到当前的工作目录上
    * git pull origin master
* 提交修改至远程
     * git push origin master
