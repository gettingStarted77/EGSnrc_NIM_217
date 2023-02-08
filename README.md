一 VMware Workstation 17 Pro for windows安装

- 官方网站下载（[https://www.vmware.com/go/getworkstation-win]()）
  
- 激活码二选一，失效可淘宝购买
  
  - MC60H-DWHD5-H80U9-6V85M-8280D
    
  - NZ4RR-FTK5H-H81C1-Q30QH-1V2LA
    

# 二 ubuntu虚拟机安装

- 查看本机cpu线程数，虚拟分配线程数应小于本机，VMware最大支持32线程
  
- 查看本机内存，分配内存应小于本机，上不封顶
  
- 下载ubuntui desktop 22.04 LTS
  
- 开机后修改清华镜像源（[ubuntu | 镜像站使用帮助 | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/)），以提高软件下载速度
  
  1. 更新本地包缓存
    
    `sudo apt update `
    
    命令不仅更新存储库索引，还告知存储库中是否可用软件以及有多少新版本可用.
    
  2. 查找与安装包说明
    
    - 使用apt-cache搜索包名
    
    `apt-cache search package_name`
    
    - 使用apt-cache搜索关键字
    
    `apt-cache search “package_keyword”`
    
    - 使用apt-cache显示有关程序包的基本信息
    
    `apt-cache show package_name`
    
    - 安装程序包
    
    `sudo apt install package_name`
    
  3. apt 命令
    
    ![image](https://github.com/gettingStarted77/EGSnrc_NIM_217/blob/main/2023-02-04-18-32-34-image.png)
    
  4. VMware虚拟机安装ubuntu20.04与Windows如果不能相互复制与粘贴
    
    `sudo apt install open-vm-tools open-vm-tools-desktop`
    
    安装后重启
    

# 三 EGSnrc官网（[What is EGSnrc? | EGSnrc](https://nrc-cnrc.github.io/EGSnrc/)）

- EGSnrc官方安装指导（[Installation overview · nrc-cnrc/EGSnrc Wiki · GitHub](https://github.com/nrc-cnrc/EGSnrc/wiki/Installation-overview)）
  
- 安装prerequisite software
  
  > 一条安装： `sudo apt install gfortran gcc g++ make tk grace libmotif-dev qt5-qmake qtbase5-dev at`
  
  1. a Fortran compiler (preferably `gfortran`)
    
    `sudo apt install gfortran`
    
  2. a C compiler (preferably `gcc`)
    
    > 作为gfortran的依赖已被安装
    
  3. a C++ compiler (preferably `g++`)
    
    `sudo apt install g++`
    
  4. the GNU `make` utility
    
    `sudo apt install make`
    
  5. *optional:* the Tcl/Tk interpreter and widget toolkit, version 8.0 or later
    
    > 可视化界面，如beamntc_gui
    
    `sudo apt install tk`
    
  6. *optional:* the Grace plotting tool (providing the `xmgrace` command), version 5.0 or later
    
    > 终端可输入xmgrace单独使用，作图工具
    
    `sudo apt install grace`
    
  7. *optional:* Open Motif development package, to compile dosxyz_show (e.g. `libmotif-dev`)
    
    `sudo apt install libmotif-dev`
    
  8. *optional:* the Qt4 or Qt5 development tools (e.g. `qt5-default` and `qt5-qmake`), to re-compile the Qt GUIs
    
    `sudo apt install qt5-qmake qtbase5-dev`
    
  9. *optional:* a job scheduler of your choice (e.g. the package `at`), for parallel processing
    
    > 多线程
    
    `sudo apt install at`
    
- 下载EGSnrc源码
  
  > 需要下载git：`sudo apt install git`
  
  `git clone https://github.com/nrc-cnrc/EGSnrc.git`
  
- 安装
  
  > HEN_HOUSE: Points to location of the EGSnrc system
  > 
  > EGS_HOME: Points to user’s working directory, where applications are copied
  
  - 使用gui安装
    
  - 使用脚本安装
    

- 检查安装
  
  1. env
    
  2. alias
    
  3. 查看EGSnrc可执行文件
