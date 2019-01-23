#### LEFT OUTER JOIN 碰上 ！= 

关联的时候发现
```sql
SELECT 
	*
FROM A 
LEFT OUTER JOIN B 
	ON A.id = B.id 
	AND A.date  != B.date

```
数据刷出来总是不正确的，许多错误数据。
后来改成了如下的方式：
```sql
SELECT 
	*
FROM A 
LEFT OUTER JOIN B 
	ON A.id = B.id
WHERE 1=1
	AND A.date  != B.date

```