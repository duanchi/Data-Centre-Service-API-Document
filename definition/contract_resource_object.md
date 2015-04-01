# 4.1.5.2 Contract_Resource Object


> 合约计划资源对象


### 定义

---
```
Class Contract_Resource extend StdClass {
    public Product_Data product;
    public enum type;
    public string model;
    public string costs;
    public string price;
    public int term;
    public string subsidy;
    public string deposit;
    public string grants;
    public string prestored;
    public string minimum_consumption;
    public string return_proportion;
};
```
---


### 属性


* #### product

> type :　`object(Product_Data)`

> desc : 当前用户主产品信息

> value : see [4.1.4.2 Product_Data Object](/definition/product_data_object.html#4142-product_data-object)


* #### type

> type :　`enum`

> desc : 当前用户合约计划类型

> value :

> - `0` 存费送费

> - `1` 购手机送话费

> - `2` 存话费送手机

> - `3` 存费送业务

> - `4` 单卡


* #### model

> type :　`string`

> desc : 当前用户合约计划的资源型号

> value : 资源型号


* #### costs

> type :　`string`

> desc : 当前用户合约计划的资源成本

> value : 资源成本


* #### price

> type :　`string`

> desc : 当前用户合约计划的资源购买价格

> value : 资源购买价格


* #### term

> type :　`int`

> desc : 当前用户合约计划的协议时长(月)

> value : 协议时长


* #### subsidy

> type :　`string`

> desc : 当前用户合约计划业务补贴金额

> value : 补贴金额


* #### deposit

> type :　`string`

> desc : 当前用户合约计划业务押金

> value : 押金


* #### grants

> type :　`string`

> desc : 当前用户合约计划业务赠款金额

> value : 赠款金额


* #### prestored

> type :　`string`

> desc : 当前用户合约计划业务预存款金额

> value : 预存款金额


* #### minimum_consumption

> type :　`string`

> desc : 当前用户合约计划业务最低消费金额

> value : 最低消费金额


* #### return_proportion

> type :　`string`

> desc : 当前用户合约计划业务按月返还比例

> value : 按月返还比例



### DUMP

```
object(Contract_Resource) {
    "product" : object(Product_Data) {
        ...
    },
    "type" : enum(1),
    "model" : string("xxp2m"),
    "costs" : string("1899"),
    "price" : string("2699"),
    "term" : int(24),
    "subsidy" : string("800"),
    "deposit" : string("0"),
    "grants" : string("800"),
    "prestored" : string("1899"),
    "minimum_consumption" : string("68"),
    "return_proportion" : string("8%")
}
```
