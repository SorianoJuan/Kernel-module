OBJECTS := encrypter.o ioctl.o

obj-m := encrypter.o 
fifo-objs := $(OBJECTS)

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean
