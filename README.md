## ˵��
1. ��`STM32V6`��������ڲ�`RAM`ģ���`U��`��

## ע��
1. ͨ��`CubeMx`���ɴ������Ҫ�༭[usbd_storage_if.c](./USB_DEVICE/App/usbd_storage_if.c)�е�������Ϣ��
```c
// STM32F429 ���� RAM 192KB(128 RAM + 64 CCM)���������� U�� ��СΪ 50KB
#define STORAGE_BLK_NBR     100
#define STORAGE_BLK_SIZ     512
```
2. �����ǽ�`RAM`ģ���`U��`����`RAM`��Ϣ���粻���棬����ÿ�γ������в��͵������Ӻ󣬶�ֻ�ܿ���һ��Ϊ��ʽ�����̷�����Ҫ�Ƚ��и�ʽ�������ܺ�`U��`һ������ʹ�ã�
3. ���������õ�`RAM`��СΪ`50KB`����ʵ����`windows`�̷��¿�����ȴ��`30KB`��Ӧ�����ļ�ϵͳ������Ҫһ���Ŀռ�(`20KB`)��
4. �����̱���ʹ��`ARM Compiler V5`���������������`U��`��ʹ��`ARM Compiler V6`���У�