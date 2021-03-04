# element

### 元素
| 元素名   | 作用                         | 备注                                                  |
|----------|------------------------------|-------------------------------------------------------|
| textarea | 多行可编辑纯文本元素         |                                                       |
| label    | 表示用户界面中某个元素的说明 | `for`属性绑定其他元素的`id`或将其他元素放入`labele`中 |
| iframe   | 嵌入新的HTML页面             |                                                       |


### CSS属性
#### resize
控制一个元素的可调整大小性，默认值`none`
##### 取值
`none`：元素不能被用户缩放  
`both`：可以在水平和垂直方向上调整元素大小  
`horizontal`：可以在水平方向上调整大小  
`vertical`：可以在垂直方向上调整大小
##### 注意
如果一个block元素的`overflow`属性被设置成`visible`，那么`resize`属性无效
##### 链接
[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/resize)

#### 