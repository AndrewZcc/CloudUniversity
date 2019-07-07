### Python 虚拟环境使用

----

1. 使用第三方包 `virtualenvwrapper` 

   * 使用该第三方包的好处：它会帮你统一管理你的虚拟环境！

   * 使用说明：

     ```shell
     #1. 创建虚拟环境
     $ mkvirtualenv my_env
     #2. 切换到某个虚拟环境
     $ workon my_env
     #3. 退出当前这个虚拟环境
     $ deactivate
     #4. 删除某个虚拟环境
     $ rmvirtualenv my_env
     #5. 列出 当前系统上已创建的所有虚拟环境
     $ lsvirtualenv
     #6. 快速 进入到某个虚拟环境所在的目录
     $ cdvirtualenv my_env
     
     [扩展]
     #1. 修改 默认 虚拟环境存储位置
     [windows] 修改 WORKON_HOME 这个系统环境变量的值 即可
     #2. 为某个虚拟环境 指定特定的Python版本(Python解释器)
     $ mkvirtualenv --python==C:\Python37\python.exe my_env
     ```

   