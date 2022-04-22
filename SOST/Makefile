obj-m += hello-4.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules
	rm *.o *.symvers *.order *.mod.c

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

insmod:
	sudo insmod ./hello-4.ko

rmmod:
	sudo rmmod hello-4

modinfo:
	modinfo hello-4.ko

showmessage:
	cat /var/log/syslog


