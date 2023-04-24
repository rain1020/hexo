---
title: Node.js EventEmitter
---

## Node.js EventEmitter

#### 一.定义

EventEmitter：events 模块的对象，核心功能是事件的触发和监听器的注册。

---

#### 二.属性

##### <u>_方法_</u>

1. EventEmitter() 构造函数
2. addListener(event,listener) 添加事件监听器
3. on(event,listener) 注册监听器
4. once(event,listener) 注册单次事件监听器，监听器触发后就移除
5. removeListener(event,listener) 移除指定事件的监听器
6. removeAllListeners([event]) 移除所有事件的监听器，如果指定事件，移除指定事件的所有监听器
7. listeners(event) 查询事件监听器
8. emit(event,args) 触发事件

##### <u>_事件_</u>

1. newListener(event,listener) 添加监听器的时候触发
2. removeListener(event,listener) 移除监听器的时候触发

##### <u>_继承_</u>

对象继承包括: fs,net,http

---

#### 三.应用

eg1:

```
var EventEmitter = require('events').EventEmitter;
var event = new EventEmitter()
let callback =  function() {
  console.log('event 事件触发')
}
event.on('event',callback)
conslo.log(event.listenerCount('event')+'个监听器')
event.emit('event')
eventEmitter.removeListener('event', callback);
conslo.log(event.listenerCount('event')+'个监听器')
```

执行结果：

> event 事件触发
> 1 个监听器
> 0 个监听器
