<template>
  <div>
    <a-button @click="current = 'home'">首页</a-button>
    <a-button @click="current = 'table'">表格</a-button>
    <a-button @click="current = 'form'">表单</a-button>
    <home-com v-if="current === 'home'"></home-com>
    <table-com v-if="current === 'table'"></table-com>
    <form-com v-if="current === 'form'"></form-com>
  </div>
</template>

<script>
import HomeCom from './home'
import TableCom from './table'
import FormCom from './form'
export default {
  name: 'index',
  components: {
    HomeCom,
    TableCom,
    FormCom
  },
  data() {
    return {
      current: 'home'
    };
  },
  methods: {},
}
</script>
<style scoped>

</style>