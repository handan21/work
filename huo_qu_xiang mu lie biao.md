
# 获取项目列表

* ** api : [ /api/get_application_list]( /api/get_application_list)** 

* **method : GET/POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| cooperation_type  | int | no | 合作类型 1为91合作，2为非91合作|


* **return : json**

```
{
    "status" : true/false
    “code”:null
    "msg" : null /暂无数据 
    "data" : [
        {
            "app_id"：<int>, //项目id
            "house_name" : <stirng>, //楼盘名称
            "hid" : <int>, //楼盘ID
            "city_en" : <stirng> , //楼盘所在城市
            "area" : <stirng> ,//楼盘所在的区域
            "price" ：<stirng> //价格
            "price" ：<stirng> //价格
            "price" ：<stirng> //价格
            "price" ：<stirng> //价格
            "price" ：<stirng> //价格
            "price" ：<stirng> //价格
            "price" ：<stirng> //价格
            "price" ：<stirng> //价格
            "price" ：<stirng> //价格
            "price" ：<stirng> //价格
        }
    ]
}

```
* **返回错误代码 code 列举**

```
 暂无

```
* **订单状态**

|【滴滴】状态码|描述|
|--|--|
|300| 	等待应答|
|311 |	订单超时|
|400 |	等待接驾|
|410 |	司机已到达|
|500 |	行程中|
|600 |	行程结束|
|610 |	行程异常结束|
|700| 	已支付 |

* **requirement : **
* **provider : 码上专车系统**
