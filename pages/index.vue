<template>
  <div>
    <h3>index page</h3>
    <!-- 组件自动导入 -->
    <BaseFooButton></BaseFooButton>
    <!-- 组件懒加载 -->
    <h1>Mountains</h1>
    <LazyMountainsList v-if='show'></LazyMountainsList>
    <button v-if="!show" @click="show = true">显示列表</button>
    <br/>

    <div v-for="todo in todos" :key="todo.id">
      <input type="checkbox" v-model="todo.completed">
      <strong>{{todo.title}}</strong>
    </div>
    <br/>

    <button @click="counter++">+</button>
    {{counter}}
    <button @click="counter--">-</button>

    <!--普通路由-->
    <NuxtLink to="/detail">Detail Page</NuxtLink>
    <br/>
    <NuxtLink to="/helloWorld">hello Page</NuxtLink>
    <br/>
    <!--嵌套路由-->
    <NuxtLink to="/parent/child">parent page</NuxtLink>
    <br/>
    <!--动态路由-->
    <NuxtLink to="/user-admin/1">user page</NuxtLink>
  </div>
</template>
<script setup lang="ts">
  import { ref } from 'vue'
  import { useCounter } from '~~/composables/useCounter'
  const show = ref(false)
  // const {data:todos} = await useAsyncData('todos',()=>$fetch('/api/todo')) 
  const {data:todos}:any = await useFetch('/api/todo',{
    transform(input:{data:[]}){
      return input.data
    }
  })
  console.log(todos.value)
  //声明ssr友好状态
  let counter = useCounter()
</script>