# **MONTH()**

## **函数说明**

`MONTH()`函数返回了给定日期的月份（从1到12）。


## **函数语法**

```
> MONTH(date)
```
## **参数释义**
|  参数  | 说明  |
|  ----  | ----  |
| date  | 必要参数，需要提取月份的日期 |



## **示例**


```sql
> drop table if exists t1;
> create table t1(a date);
> insert into t1 values('20211223');
> insert into t1 values('2021-12-24');

> select month(a) from t1;
+----------+
| month(a) |
+----------+
|       12 |
|       12 |
+----------+
```

## **限制**

目前只支持`yyyy-mm-dd` 和 `yyyymmdd`的数据格式。  

MatrixOne目前只支持在查询表的时候使用函数，不支持单独使用函数。