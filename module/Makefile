obj-m += pat_dealloc.o
PWD := $(CURDIR)

build:
	make -C /usr/src/linux M=$(PWD) modules

clean:
	make -C /usr/src/linux M=$(PWD) clean

load: build unload
	sudo insmod pat_dealloc.ko

unload:
	-sudo rmmod pat_dealloc
