# 鲁班猫2 rk3568
野火的linux驱动git仓库练习使用
编译内核源码时要记得module源码单独编译,否则会缺失依赖
export  ARCH  CROSS_COMPILE		//导出环境变量确保编译器一致，也避免了重复调用

与内核耦合时尽量后缀使用.ko如果出现错误不会导致内核出现 panic 错误，如果集成到内核，出错了就会出现 panic。
```shell
#鲁班猫风扇控制pwm代码
echo 0 > /sys/class/pwm/pwmchip0/export
echo 1000000 > /sys/class/pwm/pwmchip0/pwm0/period
echo 500000 > /sys/class/pwm/pwmchip0/pwm0/duty_cycle
echo "normal" > /sys/class/pwm/pwmchip0/pwm0/polarity
echo 1 > /sys/class/pwm/pwmchip0/pwm0/enable
```


