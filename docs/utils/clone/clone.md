<script setup>
import clone from './clone.vue'
import cloneDeep from './cloneDeep.vue'
import hasOwnProp from './hasOwnProp.vue'
</script>

# 浅拷贝/深拷贝、判断对象自身属性中是否具有指定的属性

<ClientOnly>
  <description-popover :num="3" :tagNameList="['浏览器','Node']" />
</ClientOnly>

## clone

<ClientOnly>
  <description :isShowIcon="false" description="浅拷贝/深拷贝" /> 
</ClientOnly>

### 参数

- 接收两个参数，第一个参数 `val` ，第二个参数 `deep` ，返回拷贝后的值

| **参数属性** | **说明**                 | **类型**  | **默认值** |
| ------------ | ------------------------ | --------- | ---------- |
| `val`        | 需要拷贝的值             | `any`     | -          |
| `deep`       | 是否深拷贝（默认浅拷贝） | `boolean` | `false`    |

### 基础用法

<ClientOnly>
  <clone />
</ClientOnly>
<details>

<summary>查看代码</summary>

<<< @/utils/clone/clone.vue

</details>

## cloneDeep

<ClientOnly>
  <description :isShowIcon="false" description="深拷贝" /> 
</ClientOnly>

### 参数

- 接收一个参数 `val` ，返回拷贝后的值

| **参数属性** | **说明**     | **类型** |
| ------------ | ------------ | -------- |
| `val`        | 需要拷贝的值 | `any`    |

### 基础用法

<ClientOnly>
  <cloneDeep />
</ClientOnly>
<details>

<summary>查看代码</summary>

<<< @/utils/clone/cloneDeep.vue

</details>

## hasOwnProp

<ClientOnly>
  <description :isShowIcon="false" description="判断对象自身属性中是否具有指定的属性" /> 
</ClientOnly>

### 参数

- 接收两个参数，第一个参数 `obj` ，第二个参数 `key` ，返回值类型 `boolean`

| **参数属性** | **说明**     | **类型**           |
| ------------ | ------------ | ------------------ |
| `obj`        | 要判断的对象 | `object`           |
| `key`        | 指定的属性   | `string`、`number` |

### 基础用法

<ClientOnly>
  <hasOwnProp />
</ClientOnly>
<details>

<summary>查看代码</summary>

<<< @/utils/clone/hasOwnProp.vue

</details>

:::tip
浅拷贝：只拷贝一层，更深层次对象级别的只会拷贝引用`地址`（不影响`基本数据类型`）  
深拷贝：指源对象与拷贝对象互相独立，其中任何一个对象的改动都不会对另外一个对象造成影响，每一层都会拷贝（既不影响`基本数据类型`，又不影响`引用数据类型`）
:::
