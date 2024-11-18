KERNEL_DIR=../../kernel/

ARCH=arm64
CROSS_COMPILE=aarch64-linux-gnu-
export  ARCH  CROSS_COMPILE

obj-m := led_pdev.o led_pdrv.o

#$(MAKE)确保不会丢失当前环境变量
#$(KERNEL_DIR)是一个变量，表示源码所在路径
#M=$(CURDIR) 参数告诉内核构建系统，外部模块的源码路径，$(CURDIR) 是一个 Makefile 内置变量，表示 当前目录。
#modules是内核构建目标
all:
	$(MAKE) -C $(KERNEL_DIR) M=$(CURDIR) modules
modules clean:
	$(MAKE) -C $(KERNEL_DIR) M=$(CURDIR) clean	
