#递归算法实现深拷贝
```javascript

       function getClass(o) {
            return Object.prototype.toString.call(o).slice(8, -1);//判断传入的数据类型
        }

        function deepCopy(o) {
            var result, oClass = getClass(o);
            if (oClass == "Object") {
                result = {};
            } else if (oClass == "Array") {
                result = [];
            } else {
                return o;
            }
            for (var key in o) {
                var copy = o[key];
                if (getClass(copy) === 'Object' || getClass(copy) === "Array") {
                    result[key] = deepCopy(copy);
                } else {
                    result[key] = copy;
                }
            }
            return result;
        }


        var obj = {
            a: 123,
            b: [123, 234, {
                x: 0,
                y: {
                    a: 1
                }
            }]
        };

        var obj2 = deepCopy(obj);
        console.log(obj2);
        

```