## 常用的 git 命令

  1.git init ：初始化本地仓库，在该目录下生成.git目录
  2.git clone 地址 ：克隆远程仓库
  3.git status ：查看状态
  4.git add 文件 ：添加被改动的文件到暂存区
  5.git commit -m "注释内容" ：将暂存区文件实际保存到仓库
  6.git log ：查看提交内容
  7.git rm 文件 
  8.git branch -a ：查看本地及远程的所有分支
  9.ls :查看当前目录下的所有文件
  10.cd 文件 ：进入文件
  11.touch 文件 ：新建文件
  12.vim 文件 ：打开要编辑的文件
  13.ls :查看当前目录文件
  14.ll :查看当前文件夹下面所有文件包括隐藏文件
  15.pwd :可以查看当前目录位置
  16.clear :清屏


## 产生代码冲突

# 情况

     假设有两个本地仓库，分别为仓库A，仓库B
     1.在本地，两个仓库分别同时克隆同一个远程仓库。
     2.在仓库A修改了远程仓库克隆下来的文件，并提交到远程
     3.在仓库B修改同一文件，尝试提交到远程，出现冲突

# 解决

    步骤
       1.git pull （拉取远程文件）
       2.<<<<< HEAD
         本地内容
         ====
         远程内容
         >>>>>
    
         注：如要接受两个仓库修改时，删去乱码
       3.git commit -m "注释"
       4.git add 文件
       5.git commit -m "注释"
       6.git push