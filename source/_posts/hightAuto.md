---
title: 高度自适应
date: 2022-12-24
---

### 应用场景

<div align="center">
  <img src="../images/close.png" width=200 style='margin-right:100px'/>
  <img src="../images/open.png" width=200/>
</div>
```
<div v-heightAotu=[10,46]>你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好你好</div>
```

### 实现代码

```bash
  var max_height
  var min_height
  var originInnerHtml
  esport default {
    bind ( el,binding,vnode ) {
      let value = binding.value ?? []
      min_height = Math.min(parseInt(value[0]) ?? 0 )
      max_height = Math.max(parseInf(value[1]) ?? 0)
      originInnerHtml = el.innerHTML
      el.style.position = 'relative'
      if (!(min_height && max_height)) return
      el.addEventListener('click', function (event) {
      let { target } = event
      if (target instanceof HTMLSpanElement) {
        let height = 0
        let text
        var classVal = el.getAttribute('class');
        if( classVal.includes('close') ) {
          classVal = classVal.replace("close", "open");
          height = this.firstChild.scrollHeight + 20
          text = '收起'
        }else if( classVal.includes('open') ) {
          classVal = classVal.replace("open", "close");
          height = max_height
          text = '展开全部'
        }
        el.setAttribute("class", classVal);
        this.style.height = height + 'px'
        target.innerHTML = text
      }
    })
      let height = el.clientHeight
      if( height > max_height ) {
         addSpan(el)
      }
    },
    update ( el,biding ) {
      let height = el.clientHeight
      if( height > max_height ) {
        addSpan(el)
      }else {
        el.innerHTML = originInnerHtml
      }
    }
  }
  function addSpan (el) {
    let str = el.innerText
    el.classList = [...el.classList,'close'].join(' ')
    let bg_color = window.getComputedstyle(el,null).backgroundColor
    let line_height = window.getComputedstyle(el,null).lineHeight
    let movel = `<span style="
    position:absolute;
    width:150px;
    height:${line_height}px;
    bottom:0;
    right:0;
    background:linear-gradient(90deg, rgba(244,246,249,0) 0%, #f4f6f9 100% ,#f4f6f9 100%);"></span>`
    el.style.height = `${max_height}px`
    el.innerHTML = `<div style="position:relative;height:100%;overflow:hidden">${str}
    <span style="background: ${bg_color}; color:#1F80FF; position:absolute;right:1px;bottom:0px;cursor: pointer;z-index:10;">展开全部</span>${movel}</div>`
  }

```
