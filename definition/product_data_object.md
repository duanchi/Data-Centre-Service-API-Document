# 4.1.4.2. Product_Data Object


> 产品信息对象


### 定义

---
```
Class Product_Data extend StdClass {
    public string id;
    public string name;
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


* #### member

> type :　`object(User_Data)[]`

> length : 1 ... n

> desc : 当前沃家庭成员号码信息集合

> value : see [4.1.4.1 User_Data Object](/definition/user_data_object.html#4141-user_data-object)


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

> - `TRUE` 有效

> - `FALSE` 无效



### DUMP

```
object(WoFamily_Data) {
    "product" : object(Product_Data) {
        ...
    },
    "master" : object(User_Data){
        ...
    },
    "member" : [
        object(User_Data){
            ...
        },
        ...
    ],
    "accept_time" : datetime(2012-10-11 15:36:09),
    "effect_time" : datetime(2012-11-01 00:00:00),
    "expire_time" : datetime(2015-11-30 23:59:59),
    "enabled" : TRUE,
    "group_enabled" : TRUE
}
```
