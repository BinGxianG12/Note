# 13 事件

> 什么是事件，JavaScript与HTML之间的交互是通过**事件**实现的

## 13.1 事件流

### 13.1.1 事件冒泡

> 事件开始是由最具体的元素接受，然后逐级向上传播到较为不具体的节点

![image-20191030185818865](/home/han/.config/Typora/typora-user-images/image-20191030185818865.png)

### 13.1.2 事件捕获

> 与事件冒泡相反

![image-20191030185944423](/home/han/.config/Typora/typora-user-images/image-20191030185944423.png)

> 大多数时间使用事件冒泡

### 13.1.3 DOM事件流

1. 事件捕获阶段
2. 处于目标阶段
3. 事件冒泡阶段

![image-20191030190220136](/home/han/.config/Typora/typora-user-images/image-20191030190220136.png)

## 13.2 事件处理程序

> 事件处理程序的名字以on开头，因此click事件的事件处理程序就是onclick，为事件指定处理程序的方式有好几种

### 13.2.1 HTML事件处理程序

在js中定义被调用的函数 ，这样函数就有一个局部变量event，也就是事件对象。通过这个event变量，可以直接访问事件对象 等等等等368页，待完善//todo

### 13.2.2 DOM0级事件处理程序

![image-20191030191528344](/home/han/.config/Typora/typora-user-images/image-20191030191528344.png)

此时，函数的this指向当前元素

![image-20191030191641699](/home/han/.config/Typora/typora-user-images/image-20191030191641699.png)

通过把事件处理程序设置为null将其删除

### 13.2.3 DOM2级事件处理程序

> DOM2级事件定义了两个方法，用于处理指定和删除事件处理程序 `addEvevtListener()` 和 `removeEvevtListener()`

以上两个函数接受3个参数：

1. 处理事件的事件名
2. 作为处理事件的函数
3. 一个布尔值（true表示在捕获阶段进行调用， false表示在冒泡阶段进行调用）

![image-20191030192157930](/home/han/.config/Typora/typora-user-images/image-20191030192157930.png)

可以添加多个事件处理程序

![image-20191030192241269](/home/han/.config/Typora/typora-user-images/image-20191030192241269.png)

### 13.2.4 IE事件处理程序

`attachEvent()` 和 `derachEvebt()`接受两个参数

1. 事件处理程序名称
2. 事件处理程序函数

### 13.2.5 跨浏览器的事件处理程序





## 13.3 事件对象

> 触发事件就会产生一个事件对象，这个对象里面包含着所有与事件有关的信息

### 13.3.1 DOM中的事件对象

![image-20191030192803352](/home/han/.config/Typora/typora-user-images/image-20191030192803352.png)

无论是使用哪种方法，DOM0级或者DOM2级都会传入event对象

### 13.3.2 IE中的事件对象

### 13.3.3 跨浏览器的事件对象





## 13.4 事件类型

### 13.4.1 UI事件

1. load事件

![image-20191030193405128](/home/han/.config/Typora/typora-user-images/image-20191030193405128.png)