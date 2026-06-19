---
tags:
  - 哈希表
  - 时间戳
---
setAll功能，就是将当前哈希表中存在的value都改为一样的值，后续新加的数据不影响

要实现这个功能可以加一个**时间戳**来解决

![Pasted image 20260203154408](../../attachment/Pasted%20image%2020260203154408.png)
用cnt来标记每次操作的时间，setalltime表示执行setall操作的时间，
	如果数据的cnt\<setalltime那么说明，在执行setall操作时，这个数据一定在哈希表中存在，所以在get时，返回的数据就是setallvalue；
	如果数据的cnt\>setalltime那么说明，在执行setall操作时，这个数据在哈希表中还不存在，所以在get时，返回的数据就是他的value；

## 代码
![500](../../attachment/Pasted%20image%2020260203155133.png)
![Pasted image 20260203155209](../../attachment/Pasted%20image%2020260203155209.png)
![Pasted image 20260203155224](../../attachment/Pasted%20image%2020260203155224.png)
![Pasted image 20260203155239](../../attachment/Pasted%20image%2020260203155239.png)
测试连接：https://www.nowcoder.com/practice/7c4559f138e74ceb9ba57d76fd169967
