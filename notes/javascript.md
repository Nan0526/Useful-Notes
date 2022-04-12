# Javascript (ES6)
### get method
在JS的class里面经常会看到get method，比如：   
```
class Point {
    constructor(x, y) {
        this.x = x;
        this.y = y;
    }
    static get ZERO() {
        return new Point(0, 0);
    }
}
```
这里的get我感觉有点类似于python里面的`@property` decorator, 可以直接call `Point.ZERO` 来获取    

### static method
JS里的static method和JAVA里的差不多，不需要instanciate 就可以直接call    
