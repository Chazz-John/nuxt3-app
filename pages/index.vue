<template>
  <div>
    <h3>index page</h3>
    <!--普通路由-->
    <NuxtLink to="/detail">Detail Page</NuxtLink>
    <br/>
    <!--动态路由-->
    <NuxtLink to="/user-admin/1">user page</NuxtLink>
    <br/>
    <!--嵌套路由-->
    <NuxtLink to="/parent/child">parent page</NuxtLink>
  </div>
</template>
<script setup>
</script>
