# 4.1.4.5. Contract_Data Object


> 合约信息服务内容对象


### 定义

---
```
Class Contract_Data extend StdClass {
    public Contract_Resource resource;
    public enum province;
    public enum city;
    public datetime accept_time;
    public datetime effect_time;
    public datetime expire_time;
    public boolean enabled;
    public enum status;
};
```
---


### 属性


* #### resource

> type :　`object(Contract_Resource)`

> desc : 当前用户合约信息服务资源对象

> value : see [4.1.5.2 Contract_Resource Object Object](/definition/contract_resource_object.html#4152-contract_resource-object)


* #### province

> type :　`enum`

> desc : 当前用户合约计划的所属省

> value : 所属省，see [B-SDM Provice Code](/appendix/b-sdm_code.html/#province-code)


* #### city

> type :　`enum`

> desc : 当前用户合约计划的所属地市

> value : 所属地市，see [B-SDM City Code](/appendix/b-sdm_code.html/#city-code)


* #### master

> type :　`object(User_Data)`

> desc : 当前沃家庭主号码信息

> value : see [4.1.4.1 User_Data Object](/definition/user_data_object.html#4141-user_data-object)


* #### accept_time

> type :　`datetime`

> desc : 当前用户合约计划业务受理时间

> value : 业务受理时间


* #### effect_time

> type :　`datetime`

> desc : 当前用户合约计划业务生效时间

> value : 业务生效时间


* #### expire_time

> type :　`datetime`

> desc : 当前用户合约计划业务失效时间

> value : 业务失效时间


* #### enabled

> type :　`boolean`

> desc : 当前用户合约计划业务是否有效

> value :

> - `TRUE` 有效

> - `FALSE` 无效


* #### status

> type :　`enum`

> desc : 当前用户合约计划业务状态

> value :

> - `USING` 在用

> - `INEFFECTIVE` 未开始使用



### DUMP

```
object(Contract_Data) {
    "resource" : object(Contract_Resource) {
        ...
    },
    "province" : enum(18),
    "city" : enum("188"),
    "accept_time" : datetime(2012-10-11 15:36:09),
    "effect_time" : datetime(2012-11-01 00:00:00),
    "expire_time" : datetime(2015-11-30 23:59:59),
    "enabled" : TRUE,
    "status" : enum(USING)
}
```
