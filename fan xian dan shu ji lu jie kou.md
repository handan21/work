
# 返现记录接口


* **描述**
```
测试地址 10.207.0.175  admin.f.leju.com
正式地址 admin.f.leju.com
```

* ** api : [/api/return_money_record](//api/return_money_record)** 

* **method : POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
|hid |int|yes|楼盘id
|return_money_num|int|yes| 返现单数 |
|return_money_time |int|yes|返现时间|

* **return : json**

```
  {
      // 调⽤成功返回true，失败返回false
      status: true/false,
      // 状态描述
      msg: '成功或失败的状态描述，⽂字信息'
  }
```
* **返回错误代码 code 列举**

```
无
```


* **requirement : 滴滴约车系统**
* **provider : 跟单系统**
