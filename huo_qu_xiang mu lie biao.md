
# 获取项目列表信息


* **描述**
```
测试地址 58.83.214.101  admin.f.leju.com
正式地址 admin.f.leju.com
```


* ** api : [ /api/get_applications]( /api/get_applications)** 

* **method : GET/POST**

* **charset : UTF-8**

* **params : **

| 名称|类型| 必选 | 描述|
| -- | -- | -- | -- |
| cooperation_type  | int | no | 合作类型 1为91合作，2为非91合作|
| returnmoney_time  | int | no | 查看什么时候的返现单数 (时间戳)|
| house_name  | string | no | 楼盘名称 |
| pricerange  | int | no | 价格区域 (编号)|
| housetype  | int | no | 户型 (编号)|
| area  | string | no | 区域 |
| address  | string | no | 楼盘地址 |
|limit|int|no|每页显示多少条数据 （可选参数 , 不填则所有） |
|page|int|no|页码 从1 开始  （可选参数 和 limit 一同使用）|
| callback | string | no | jsonp 回调函数名称 |


* **return : json/jsonp**

```
{
    "status" : true/false
    “code”:null
    "msg" : null /暂无数据 
    "data" : [
        cnt  : total
        item ： 
            {
                "app_id"：                  <int>,          //项目id
                "house_name" :              <stirng>,       //楼盘名称
                "hid" :                     <int>,          //楼盘ID
                "city_en" :                 <stirng> ,      //楼盘所在城市
                "area" :                    <stirng> ,      //楼盘所在的区域
                "address" :                 <stirng>,       //楼盘地址
                "price" ：                  <stirng>,       //价格
                "housetype" ：              <stirng>,       //户型
                "cooperation_start_time" ： <datetime>,     //合作起始时间
                "cooperation_end_time" ：   <datetime>,     //合作结束时间
                "cooperation_type" ：       <int>,          //合作类型
                "month_returnmoney_num" ：  <int>,          //当月返现单数
                "surplus_returnmoney_num" ：  <int>,        //当月剩余返现单数
                ...
            }
    ]
}

```
* **返回错误代码 code 列举**

```
 暂无

```

* **requirement : **
* **provider : 网盟系统**
