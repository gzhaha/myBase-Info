#Running myBase 7.x in 64bit Ubuntu

Starting from 7.x, mybase can run in Linux system. Based on the [Online Manual](http://www.wjjsoft.com/mybase_v7_docs.html#H3_3665), 32-bit library need to be installed properly first before running myBase in 64bit Linux system.

##The process to install ia32-libs in Ubuntu 15.04 desktop amd64
As the latest version of Ubuntu does not use ia32-libs, you will need to add the old source and delete the old source after installation of the ia32-libs.   

Before changing the `sources.list`, you may also consider a backup of the original sources.list first.

Create `install-ia32.sh` with the below codes.

	cd /etc/apt/sources.list.d
	echo "deb http://archive.ubuntu.com/ubuntu/ precise main restricted universe multiverse" >ia32-libs-raring.list
	apt-get update
	apt-get install ia32-libs
	rm ia32-libs-raring.list
	apt-get update

Run `sudo install-ia32.sh` from terminal

Once finished, you can run myBase directly by double click the icon.