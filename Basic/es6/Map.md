## 理解ES6中的Map

##### Map是Es6中新增的数据结构，类似于对象，与普通对象的key必须是字符串或者数字，Map中的key可以是任意的数据类型
```javascript
    const map = new Map();
    const obj = {
        name: 'obj'
    }
    map.set(obj, 'ok')
    map.get(obj) // 'ok'
```
##### Map 实例的属性和方法如下：
- size(): 获取成员的数量
- set(): 设置成员key和value
- get(): 获取成员属性值
- has(): 判断成员是否存在
- delete(): 删除成员
- clear(): 清空所有成员
##### Map 实例的遍历方法如下:
- keys(): 返回键名
- values(): 返回键值
- entries(): 返回所有成员
- forEach(): 遍历所有成员

