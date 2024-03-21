
```markdown
# Pagination 
由原生 JavaScript 实现的页面分页器，不依赖任何第三方库。

- 包含编译后的 TypeScript 版本。
- 包含编译后的 Scss 样式文件。



## 使用

```javascript
const pagination = new Pagination({
    element: '#pagination-container',
    type: 1,
    pageIndex: 1,
    pageSize: 10,
    pageCount: 9,
    total: 100,
    prevText: '上一页',
    nextText: '下一页',
    jumper: false,
    singlePageHide: true,
    disabled: false,
    currentChange: function(index) {
        console.log('当前页码：', index);
    }
});
```

## 参数

- `element` (string): 容器的选择器，用于放置分页组件。
- `type` (number): 样式类型。1：带背景颜色 2：不带背景颜色
- `pageIndex` (number): 当前页码。
- `pageSize` (number): 每页显示数量。
- `pageCount` (number): 按钮数量。
- `total` (number): 总条数。
- `prevText` (string): 上一页按钮显示的文字。
- `nextText` (string): 下一页按钮显示的文字。
- `jumper` (boolean): 是否显示输入框跳转功能。
- `singlePageHide` (boolean): 是否在单页时隐藏分页控件。
- `disabled` (boolean): 是否禁用分页控件。
- `currentChange` (function): 按钮事件回调，接收当前页码作为参数。

## 示例

```html
<div id="pagination-container"></div>

js：
const pagination = new Pagination({
    element: '#pagination-container',
    type: 1,
    pageIndex: 1,
    pageSize: 10,
    pageCount: 9,
    total: 100,
    prevText: '上一页',
    nextText: '下一页',
    jumper: false,
    singlePageHide: true,
    disabled: false,
    currentChange: function(index) {
        console.log('当前页码：', index);
    }
});
```

## 事件

- `currentChange(index)`: 当前页码发生变化时触发的回调函数。