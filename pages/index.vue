<template>
  <div>
    <h3>index page</h3>
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
