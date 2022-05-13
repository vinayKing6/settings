#安装ubuntu20.04:
    设置-程序与功能-打开虚拟机、windows sub system for linux
    #powershell:
        wsl -l -v : 查看linux版本以及运行状态
    
    #下载安装版本，双击appx文件安装

#迁移ubuntu(wsl 默认C盘)：
    wsl -l -v : 查看虚拟机名字、运行状态
    wsl --shutdown ：关闭所有虚拟机
    wsl --export <虚拟机名字> <虚拟机导出文件路径> 如 wsl --export Ubuntu E:\wsl_for_ubuntu\wsl_ubuntu.tar
    wsl --unregister <虚拟机名字> ：删除C盘虚拟机
    wsl --import Ubuntu <虚拟机安装路径> <虚拟机导出文件路径> --version 2 如：wsl --import Ubuntu E:\wsl\Ubuntu2004\ E:\wsl_for_ubuntu\wsl_ubuntu.tar --version 2 （此时安装路径会生成虚拟镜像盘 ext4.vhdx)
    ubuntu config --default-user <username> (不然执行ubuntu是root用户) 如：ubuntu config --default-user vinay

        