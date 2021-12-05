<template>
  <div>
    <NuxtLayout name="custom">
      <template #title>
        <div>
          <h1>helloWorld</h1>
        </div>
      </template>
      <template #default>
        <div>
          content
        </div>
      </template>
    </NuxtLayout>
  </div>
</template>
<script>
// export default {
//   //设置自定义页面模板属性
//   layout:'custom'
// }
export default {
  //手动设置布局页
  layout:false
}
</script>