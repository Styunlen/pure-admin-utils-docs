<script setup>
import global from './global.vue'
</script>

# useGlobal

<ClientOnly>
  <description description="获取实例中全局property" :tagNameList="['Vue3']"  /> 
</ClientOnly>

## 基础用法

<ClientOnly>
  <global />
</ClientOnly>
<details>

<summary>查看代码</summary>

<<< @/hooks/useGlobal/global.vue

</details>

## 返回值或方法

- 返回 [`globalProperties`](https://vuejs.org/api/application.html#app-config-globalproperties)
