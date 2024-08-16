## 说明
1. 将`STM32V6`开发板的内部`RAM`模拟成`U盘`；

## 注意
1. 通过`CubeMx`生成代码后，需要编辑[usbd_storage_if.c](./USB_DEVICE/App/usbd_storage_if.c)中的如下信息：
```c
// STM32F429 共有 RAM 192KB(128 RAM + 64 CCM)，这里设置 U盘 大小为 50KB
#define STORAGE_BLK_NBR     100
#define STORAGE_BLK_SIZ     512
```
2. 由于是将`RAM`模拟成`U盘`，而`RAM`信息掉电不保存，所以每次程序运行并和电脑连接后，都只能看到一个为格式化的盘符，需要先进行格式化，才能和`U盘`一样正常使用；
3. 代码中设置的`RAM`大小为`50KB`，但实际在`windows`盘符下看到的却是`30KB`；应该是文件系统本身需要一定的空间(`20KB`)；
4. 本工程必须使用`ARM Compiler V5`编译才能正常挂载`U盘`，使用`ARM Compiler V6`不行！
