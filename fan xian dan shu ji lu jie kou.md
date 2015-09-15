
# 推送返现记录接口


* **描述**
```
测试地址 58.83.214.101  admin.f.leju.com
正式地址 admin.f.leju.com
```

* ** api : [/api/return_money_record](//api/return_money_record)** 

* **method : GET/POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|cityhid |sring|yes|cityen+楼盘id
|return_money_time |int|yes|返现时间|
| callback | sring | no | jsonp 回调函数名称 |

* **return : json/jsonp**

```
  {
      status: true/false,                    // 调⽤成功返回true，失败返回false
      msg: '成功或失败的状态描述，⽂字信息'      // 状态描述
  }
```
* **返回错误代码 code 列举**

```
无
```


* **requirement : 网盟系统**

