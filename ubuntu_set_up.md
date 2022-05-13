#更换镜像阿里云：
    sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak 备份
    sudo vi /etc/apt/sources.list
    //配置内容如下

        deb http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse 

        deb http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse 

        deb http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse 

        deb http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse 

        deb http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse 

        deb-src http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse 

        deb-src http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse 

        deb-src http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse 

        deb-src http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse 

        deb-src http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse focal

    sudo apt-get update
    sudo apt-get upgrade

#安装c/c++环境：
    sudo apt install gcc g++ make cmake

#安装neovim:
    参考neovim.md
    #detail:
        https://www.cnblogs.com/cniwoq/p/13272746.html

    #neovim配置:

        #安装node,npm:
            curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
            sudo apt install nodejs
        
        #安装clangd:
            sudo apt-get install llvm
            sudo apt-get install clang clang-10
        
        mkdir ~/.config/nvim
        mkdir ~/.config/autoload
        mkdir ~/.config/plugged
        cp init.vim ~/.config/nvim

        #配置Coc:
            CocInstall coc-marketplace
            CocList marketplace:
                安装coc-java coc-tssever coc-pyright
        
        #python配置:
            pip3 install jedi==0.17

        #c/c++配置:
            sudo apt install clangd

        #java配置:
            下载jdt.ls:https://download.eclipse.org/jdtls/milestones/1.9.0/jdt-language-server-1.9.0-202203031534.tar.gz
            export JDTLS_HOME=$HOME/gits/jdt
            复制jdt/* 到 ~/.config/coc/coc-java-data/server/

        #neovim lsp:
            npm install -g typescript typescript-language-server
            npm install -g pyright

        #安装ctags:
            下载ctags.tar.gz:https://sourceforge.net/projects/ctags/
            tar -zxvf ctags-5.8.tar.gz
            cd ctags-5.8
            sudo ./configure --prefix=/usr/bin/ctags # $PATH是你要安装的位置
            sudo make -j
            sudo make install
            export PATH=/usr/bin/ctags/bin:$PATH


#安装jdk:
    下载jdk
    解压
    输入JAVA_HOME到.bashrc/.zshrc
     export JAVA_HOME=/opt/java
     export JRE_HOME=${JAVA_HOME}/jre                    
     export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib 
     export PATH=${JAVA_HOME}/bin:$PATH

#配置tmux:
    sudo apt install tmux

    #配置oh-my-tmux:
        git clone https://github.com/Johnny4Fun/.tmux.git
        ln -s -f .tmux/.tmux.conf

#安装maven:

#配置oh my zsh:
    sudo install zsh
    https://juejin.cn/post/7023578642156355592
    下载inrc: http://mimosa-pudica.net/zsh-incremental.html
    source .zshrc

