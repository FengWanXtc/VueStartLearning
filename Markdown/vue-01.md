# 主题

## 指令

- v-bind:绑定属性
- v-on:绑定事件
  
## 组件

### 命名

1. 注册组件时使用驼峰式命名，使用时需要转成短横线

```javascript
//组件名
    components: {
        TodoItem   //或者todoItem
    }

//使用
<todo-item></todo-item>
```

1. 短横线方式使用短横线

```javascript
//组件名
    components: {
        todo-item   //或者todoItem
    }

//使用
<todo-item></todo-item>
```