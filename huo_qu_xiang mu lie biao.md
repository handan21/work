
# 获取项目列表

* ** api : [ /api/get_applications]( /api/get_applications)** 

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
            "app_id"：                  <int>,          //项目id
            "house_name" :              <stirng>,       //楼盘名称
            "hid" :                     <int>,          //楼盘ID
            "city_en" :                 <stirng> ,      //楼盘所在城市
            "area" :                    <stirng> ,      //楼盘所在的区域
            "price" ：                  <stirng>,       //价格
            "cooperation_start_time" ： <datetime>,     //合作起始时间
            "cooperation_end_time" ：   <datetime>,     //合作结束时间
            "cooperation_type" ：       <int>,          //合作类型
            "month_returnmoney_num" ：  <int>,          //每月返现单数
        }
    ]
}

```
* **返回错误代码 code 列举**

```
 暂无

```

* **requirement : **
* **provider : 码上专车系统**
