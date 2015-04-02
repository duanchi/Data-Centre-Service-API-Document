# 4.1.4.7. Terminal_Data Object


> 用户使用终端信息对象


### 定义

---
```
Class Terminal_Data extend StdClass {
    public string imei;
    public string imsi;
    public Phone_Resource phone;
    public datetime effect_time;
    public datetime expire_time = NULL;
};
```
---


### 属性


* #### imei

> type :　`string`

> desc : 当前用户终端IMEI

> value : 终端IMEI


* #### imsi

> type :　`string`

> desc : 当前用户所用手机卡IMSI

> value : 手机卡IMSI


* #### phone

> type :　`object(Phone_Resource)`

> desc : 当前用户终端对象

> value : see [4.1.5.3 Phone_Resource Object Object](/definition/phone_resource_object.html#4153-phone_resource-object)


* #### effect_time

> type :　`datetime`

> desc : 当前用户终端开始使用时间

> value : 开始使用时间


* #### expire_time

> type :　`datetime`

> desc : 当前用户终端停止使用时间

> value : 停止使用时间



### DUMP

```
object(Terminal_Data) {
    "imei" : string("4600838929919xxxxx"),
    "imsi" : string("281920040102311xxx"),
    "phone" : object(Phone_Resource){
        ...
    },
    "effect_time" : datetime(2012-11-01 00:00:00)
}
```

