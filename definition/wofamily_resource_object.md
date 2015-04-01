# 4.1.5.1. WoFamily_Resource Object


> 沃家庭融合服务资源对象


### 定义

---
```
Class WoFamily_Resource extend StdClass {
    public Product_Data product;
    public User_Data master;
    public User_data[] members;
    public enum province;
    public enum city;
    public datetime accept_time;
    public datetime effect_time;
    public datetime expire_time = NULL;
    public boolean enabled;
    public bollean group_enabled;
};
```
---


### 属性


* #### product

> type :　`object(Product_Data)`

> desc : 当前沃家庭产品信息

> value : see [4.1.4.2 Product_Data Object](/definition/product_data_object.html#4142-product_data-object)


* #### master

> type :　`object(User_Data)`

> desc : 当前沃家庭主号码信息

> value : see [4.1.4.1 User_Data Object](/definition/user_data_object.html#4141-user_data-object)


* #### members

> type :　`object(User_Data)[]`

> length : 1 ... n

> desc : 当前沃家庭成员号码信息集合

> value : see [4.1.4.1 User_Data Object](/definition/user_data_object.html#4141-user_data-object)


* #### province

> type :　`enum`

> desc : 当前沃家庭业务的所属省

> value : 所属省，see [B-SDM Provice Code](/appendix/b-sdm_code.html/#province-code)


* #### city

> type :　`enum`

> desc : 当前沃家庭业务的所属地市

> value : 所属地市，see [B-SDM City Code](/appendix/b-sdm_code.html/#city-code)


* #### accept_time

> type :　`datetime`

> desc : 当前沃家庭业务受理时间

> value : 业务受理时间


* #### effect_time

> type :　`datetime`

> desc : 当前沃家庭业务生效时间

> value : 业务生效时间


* #### expire_time

> type :　`datetime`

> desc : 当前沃家庭业务失效时间

> value : 业务失效时间


* #### enabled

> type :　`boolean`

> desc : 当前沃家庭业务是否有效

> value :

> - `TRUE` 有效

> - `FALSE` 无效


* #### group_enabled

> type :　`boolean`

> desc : 当前沃家庭号码组是否有效

> value :

> - `TRUE` 有效

> - `FALSE` 无效



### DUMP

```
object(WoFamily_Resource) {
    "product" : object(Product_Data) {
        ...
    },
    "master" : object(User_Data){
        ...
    },
    "members" : [
        object(User_Data){
            ...
        },
        ...
    ],
    "province" : enum(18),
    "city" : enum("188"),
    "accept_time" : datetime(2012-10-11 15:36:09),
    "effect_time" : datetime(2012-11-01 00:00:00),
    "expire_time" : datetime(2015-11-30 23:59:59),
    "enabled" : TRUE,
    "group_enabled" : TRUE
}
```
