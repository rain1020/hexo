## Node.js Buffer(缓冲区)

#### 一.定义

Buffer：在内存中创建一个处理二进制数据的缓存区域

#### 二.属性

##### <u>_类方法_</u>

1. Buffer.alloc(size[,fill[,encoding]]) 创建一个 size 大小的内存区域，并 fill 数值初始化，默认为 0
2. Buffer.allocUnsafe(size) 创建一个不被初始化的 size 大小的内存区域
3. Buffer.from(array) 返回一个被 array 的数值初始化的缓存区域
4. Buffer.from(arrayBuffer[,byteOffset[,length]]) 与 arrayBuffer 共享同一个内存的 Buffer
5. Buffer.from(string[,encoding]) 创建一个内容为 string 的缓存区域
6. Buffer.from(buffer) 创建一个内容与 buffer 缓存一样的新的缓存区域
7. Buffer.concat(list[,totalLength]) 创建包含 list 所有数据的新缓存

##### <u>_方法_</u>

1. write(string,[,offset[,length[],encoding]]]) 写入缓存
2. toString([encoding[,start[,end]]]) 从缓存中读取数据
3. copy(targetBuffer[,targetstart[,sourceStart[,sourceEnd]]]) 将 copy 一份 buffer 插入到 targetBuffer 的 targetStart 位置的缓存中
4. slice([start[,end]]) 创建指针指向 start，end 位置的缓存区域
5. length 返回缓存区的内存长度

#### 三.应用

eg1:

```
let buf1 = Buffer.from('我是buffer')
console.log(buf1.length)
let buf2 = Buffer.from('你是谁')
console.log(bu2.length)
let buf3 = Buffer.concat([buf1,buf2])
console.log(buf3)
consle.log(buf3.toString())
```

执行结果：

> 12
> 9
> 21
> 我是 buffer 你是谁
