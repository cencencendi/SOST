obj-m += hello-5.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules
	rm *.o *.symvers *.order *.mod.c

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

insmod:
	sudo insmod ./hello-5.ko

insmod1:
	sudo insmod ./hello-5.ko mystring="agusbejo" myshort=1122 myint=1234 mylong=87654321 myintArray=4,5

rmmod:
	sudo rmmod hello-5

modinfo:
	modinfo hello-5.ko

showmessage:
	cat /var/log/syslog


