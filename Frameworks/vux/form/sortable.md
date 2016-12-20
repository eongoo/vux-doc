# Sortable


## Props


| 名字 | 类型 | 默认 | 描述 |
|-----|-----|-----|-----|
| items | Array | 无 | 排序的内容，要有 title 属性，参考 demo `双向绑定`|
| handle | Boolean | true | 是否仅通过handle图标拖动，否则为整个item可拖动 |


## Events


| 名字 | 参数 | 描述 |
|-----|-----|-----|
| on-sort | 无 | 拖动位置变化时触发 |


## Demo


```html
<template>
 <div>
     <sortable :items.sync="items" @on-sort="onSort"></sortable>
 </div>
</template>

<script>
import { Sortable } from '../components'

export default {
 components: {
   Sortable
 },
 methods: {
   onSort () {
      console.log(this.items)
   }
 },
 data () {
   return {
     items: [{id: 'a', title: 'aaa'}, 
        {id: 'b', title: 'bbb'}, 
        {id: 'c', title: 'ccc'}, 
        {id: 'd', title: 'ddd'}, 
        {id: 'e', title: 'eee'}, 
        {id: 'f', title: 'fff'}, 
        {id: 'g', title: 'ggg'}, 
        {id: 'h', title: 'hhh'}, 
        {id: 'i', title: 'iii'}]
     }
  }
}
</script>

```