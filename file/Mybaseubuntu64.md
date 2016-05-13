#Running myBase 7.x in 64bit Linux

##Note:
**myBase 7 64bit version for Linux** is provided for download via below official website.  

> [English Version](http://www.wjjsoft.com/download.html)  
> [中文版](http://www.wjjsoft.com/mybase_cn.html#download)  

After testing, the latest version of myBase could be run directly in  

###Linux Mint 17.3 Cinnamon 64bit
* click **myBase.run** or
* run **./myBase.run** via Terminal

###Debian 8.4.0 amd64 Cinnamon Desktop
* click **myBase.run** or
* run **./myBase.run** via Terminal

###Ubuntu 16.04 Desktop amd64
* run **./myBase.run** via Terminal

###CentOS 7 x86_64 1511
* run **./myBase.run** via Terminal  
  > If you hit the error message "myBase: error while loading shared libraries: libpng12.so.0: cannot open shared object file: No such file or directory"  
  > Run command `sudo yum install libpng12` in terminal first   
	
###Fedora Workstation x86_64 23
* run **./myBase.run** via Terminal  
  > If you hit the error message "myBase: error while loading shared libraries: libpng12.so.0: cannot open shared object file: No such file or directory"  
  > Run command `sudo yum install libpng12` in terminal first   

##The process to install ia32-libs in Ubuntu 15.04 desktop amd64

**The information in this section is obsolete.** 

If you still prefer to use 32bit myBase 7 in 64bit Linux system, based on the [Online Manual](http://www.wjjsoft.com/mybase_v7_docs.html#H3_3665) the 32-bit library need to be installed properly.

As the latest version of Ubuntu does not use ia32-libs, you will need to add the old source and delete the old source after installation of the ia32-libs.   

Before changing the `sources.list`, you may also consider a backup of the original `sources.list` first.

Create `install-ia32.sh` with the below codes.

	cd /etc/apt/sources.list.d
	echo "deb http://archive.ubuntu.com/ubuntu/ precise main restricted universe multiverse" >ia32-libs-raring.list
	apt-get update
	apt-get install ia32-libs
	rm ia32-libs-raring.list
	apt-get update

Run `sudo install-ia32.sh` from terminal

Once finished, you can run myBase directly by double click the icon.