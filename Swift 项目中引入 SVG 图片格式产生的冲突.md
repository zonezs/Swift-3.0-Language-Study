# Swift 项目中引入 SVG 图片格式产生的冲突

<a name="e4bf4e62"></a>
##### SwiftSVG 库导入
存在的冲突问题，在于和SwiftColor 会产生问题，目前的解决方案是将SwiftColor 去掉或者注释了其中的代码，然后在header中添加'!'来解决这个问题<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/235650/1555988731976-f2a7c24e-42e5-462b-b38d-15ef9cf5dd9e.png#align=left&display=inline&height=278&name=image.png&originHeight=278&originWidth=576&size=196084&status=done&width=576)<br />
![image.png](https://cdn.nlark.com/yuque/0/2019/png/235650/1555988863352-f71ef60f-7b5b-42e5-b182-e909b87c1737.png#align=left&display=inline&height=265&name=image.png&originHeight=572&originWidth=1608&size=238524&status=done&width=746)
