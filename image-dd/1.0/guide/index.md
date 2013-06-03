## 综述

Image-dd是一个使图片能够支持使用滚轮放大，以及拖拽甩动的组件。

* 版本：1.0
* 基于：kissy1.20或者更高版本
* 作者：玉门


#### Image-dd的特性

* 支持代理图片的容器（或者直接注册图片到ImageDD对象）
* 以光标悬停图片的位置为中心，放大缩小图片
* 拖拽甩动，模拟物理减速直线运动

## demo

[点击访问]()

## 组件使用

kissy1.2下需要gallery的包配置：

```javascript
KISSY.config({
    packages:[
        {
            name:"gallery",
            path:"http://a.tbcdn.cn/s/kissy/",
            charset:"utf-8"
        }
    ]
});
```

kissy1.3就不需要该配置。




### 1.image-dd,初始化image-dd

```javascript
    KISSY.use('gallery/image-dd/1.0/index', function (S, ImageDD) {
        var ImageDD = new ImageDD();
    })
```
**提醒**：use()的回调，第一个参数是KISSY，第二个参数才是组件。

### 2. 使用容器代理 图片的初始化

```javascript
    KISSY.use('gallery/image-dd/1.0/index', function (S, ImageDD) {
        var ImageDD = new ImageDD(document, '.J_ImgDD');
    })
```

**提醒**：参数'.J_ImgDD' 为className, 缺省值为：'img'及为所有img标签初始化功能
    

### 3. 使用add方法， 添加一个（或多个）图片的初始化
```javascript
    KISSY.use('gallery/image-dd/1.0/index', function (S, ImageDD) {
        var ImageDD = new ImageDD();
        ImageDD.add(document, '.J_ImgDD')
    })
```



