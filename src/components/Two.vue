<template>
  <div class="two">two组件
    <ul>
      <li v-for="(item,index) in data" :key="index">{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  inject: ['message', 'data'],
  mounted () {
    console.log(this.message)
    console.log(this.data)
  }
}
</script>

<style lang='scss'>
.two {
  padding: 20px;
  border: 5px solid blanchedalmond;
}
</style>
