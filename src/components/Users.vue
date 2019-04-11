<!--1、模板：Html结构  注意template下面只可以包含一个根元素-->
<template>
  <div>
    <ul>
      <li v-for="(user,index) in users" :key="index">
        {{user}}
      </li>
    </ul>
  </div>
</template>

<!--2、行为：处理逻辑-->
<script>
  export default {
    name: 'Users',
    data () {
      return {
        users: ['张三','李四','王五']
      }
    }
  }
</script>

<!--3、样式：解决样式  注意添加scoped属性意为这部分样式只在本组件中生效-->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }
</style>
