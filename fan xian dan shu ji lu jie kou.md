
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
|city_hid |string|yes|city_en楼盘id  (如：sh126024)
|return_money_time |int|yes|申请返现时间|
|sign |string|yes|签名字符串|
| callback | string | no | jsonp 回调函数名称 |

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
* **验证签名方法**
*   @param string $params array('city_hid'=$city_en.$hid,'time'=>申请返现时的时间戳)
*  @param string $sign_key =‘3f25bc5044318bc31f0ef5ed7a927e24’
*  @return string
*  
        function getSign($params = '', $sign_key = '') {
            $params['sign_key'] = $sign_key;
            ksort($params);
            $str = '';
            foreach ($params as $k => $v) {
                if ('' == $str) {
                    $str .= $k . '=' . trim($v);
                } else {
                    $str .= '&' . $k . '=' . trim($v);
                }
            }
            $sign = md5($str);
            return $sign;
        }

* **requirement : 网盟系统**

