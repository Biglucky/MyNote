### 1. 跨平台，Windows下Git，回车符替换
报错信息：
	warning: LF will be replaced by CRLF

产生原因：
    因为跨平台，Windows与Linux中换行符不一致。导致发出这个Warning

解决方式:

```shell
   #设置转换为自动转换为 False warning不再提示。
   git config --global core.autocrlf false
```
