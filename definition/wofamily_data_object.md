# 4.1.4.x. WoFamily_Data Object


> 沃家庭融合服务信息对象


### 定义

---
```
Class WoFamily_Data extend StdClass {
    public Product_Data product;
    public User_Data master;
    public User_data[] members;
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

> type :　`object(Product)`

> desc : 当前沃家庭产品信息

> value : see [4.1.4.x WoFamily Data Object](/definition/wofamily_data_object.html#414x-wofamily_data-object)




### DUMP

```
object(Fusion_profile) {
    "wo_family" : object(WOFamily_Profile) {}
}
```






### WOFamily_Profile Object

`Class WOFamily_Profile extend Profile {}`

> - product : object(Wofamily_Product)  `沃家庭产品信息`
>   - name : string                     `沃家庭产品名称`
> - master : object(User_Profile)       `主用户对象`
> - slave : object(User_Profile)[+]     `成员用户对象`


```
object(WOFamily_Profile) {
    "product" : object(WOFamily_Product) {
        "name" : string("沃家庭91套餐"),
    },
    "master": object(User_Profile) {},
    "slave" : [
        object(User_Profile) {},
        ...
    ]
}
```
