# 4.1.4.5. Status_Data Object


> 用户在网状态信息对象


### 定义

---
```
Class Status_Data extend StdClass {
    public User_Data user;
    public Product_Data product;
    public enum status;
    public datetime effect_time;
    public datetime expire_time = NULL;
};
```
---


### 属性


* #### user

> type :　`object(User_Data)`

> desc : 当前用户信息对象

> value : see [4.1.4.1 User_Data Object Object](/definition/user_data_object.html#4141-user_data-object)


* #### product

> type :　`object(Product_Data)`

> desc : 当前当前用户所用产品信息对象

> value : see [4.1.4.2 Product_Data Object Object](/definition/product_data_object.html#4142-product_data-object)


* #### status

> type :　`enum`

> desc : 当前用户在网状态

> value :

> - `VALID` 正常

> - `INVALID` 已离网


* #### effect_time

> type :　`datetime`

> desc : 当前用户入网生效时间

> value : 入网时间


* #### expire_time

> type :　`datetime`

> desc : 当前用离网时间

> value : 离网时间



### DUMP

```
object(Status_Data) {
    "user" : object(User_Data) {
        ...
    },
    "product" : object(Product_Data){
        ...
    },
    "status" : enum(VALID),
    "effect_time" : datetime(2012-11-01 00:00:00)
}
```
