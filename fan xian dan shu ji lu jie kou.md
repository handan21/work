
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
|time|int|yes|用户专车预约时间，时间戳，指用户希望使用专车的时间|
|cityhid|string|yes|楼盘的city_en+hid 如 bj123 (验证验证码有效性的时候 必须带入)|
|location_start|string|yes|预约起始地址说明(文字)|
|location_end|string|yes|预约结束地址说明(文字)，在入口页面中， 通过业务楼盘获取 (非用户输入)|
|price|float|yes|业务系统对报名用户起止地点设定的专车费用预算价格|
|operator_name|string|yes|业务系统审核人名称|
|operator_id|int|yes|业务系统审核人id|
|project_total|int|yes|楼盘在预约看房的那一天的可提供服务的总名额|
|project_maxprice|float|yes|楼盘项目配置的单人单次可用车款上限|
|project_limit|int|yes|楼盘在预约看房的那一天的单人可报名次数限制，以手机号为准|

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
