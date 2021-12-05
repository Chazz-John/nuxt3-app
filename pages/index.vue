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
<script setup>
  import { ref } from 'vue'
  const show = ref(false)
</script>