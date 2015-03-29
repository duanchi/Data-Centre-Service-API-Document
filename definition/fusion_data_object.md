# 4.1.4.2. Fusion_Data Object

> 融合信息服务数据对象


### 定义

---
```
Class Fusion_Data extend StdClass {
    public WoFamily_Data wo_famliy = NULL;
};
```
---


### 属性


* #### wo_famliy

> type :　`object(WoFamily_Data)`

> desc : 沃家庭融合服务信息对象

> value : see [4.1.4.x WoFamily_Data Object](/definition/wofamily_data_object.html#414x-wofamily_data-object)




### DUMP

```
object(Fusion_profile) {
    "wo_family" : object(WOFamily_Profile) {}
}
```




