obj-m += hello-2.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules
	rm *.o *.symvers *.order *.mod.c

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

insmod:
	sudo insmod ./hello-2.ko

rmmod:
	sudo rmmod hello-2

showmessage:
	cat /var/log/syslog


