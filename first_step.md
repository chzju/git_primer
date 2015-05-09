* 创建代码仓库
     * git init
     * 添加文件
          * git add main.java  # 添加一个特定的文件
               * git add . # 添加所有的文件，包括子目录下的
                    * git add *.js # 添加当前目录下面的js文件
                         * git add -a # 添加所有新增、删除、修改的文件
                         * 查看仓库状态
                              * git status
                              * 提交代码
                                   * git commit main.java
                                        * git commit *.js
                                             * git commit
* 忽略某些文件
     * 编辑.gitignore文件，使用【glob】模式
