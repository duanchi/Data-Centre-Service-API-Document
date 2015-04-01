# 4.1.4.3. Fusion_Data Object

> 融合信息服务数据对象


### 定义

---
```
Class Fusion_Data extend StdClass {
    public WoFamily_Resource wo_famliy = NULL;
};
```
---


### 属性


* #### wo_famliy

> type :　`object(WoFamily_Resource)`

> desc : 沃家庭融合服务信息对象

> value : see [4.1.5.1 WoFamily_Resource Object](/definition/wofamily_resource_object.html#4151-wofamily_resource-object)




### DUMP

```
object(Fusion_Data) {
    "wo_family" : object(WoFamily_Resource) {
        ...
    }
}
```




