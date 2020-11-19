<template>
  <div>
    <a-table
      :columns="columns"
      :data-source="tableList"
      :pagination="false"
      row-key="ID"
    ></a-table>
  </div>
</template>

<script>
export default {
  name: 'table-com',
  data() {
    return {
      columns: [
        { title: "ID", dataIndex: "ID", key: "ID" },
        { title: "姓名", dataIndex: "name", key: "name" },
      ],
      tableList: []
    };
  },
  methods: {
    initTableData() {
      const element = [];
      for (let index = 1; index < 1000; index++) {
        let obj = {
          ID: 1000 + index,
          name: '郭文龙'
        }
        element.push(obj)
      }
      this.tableList.splice(0, this.tableList.length, ...element)
    }
  },
  mounted() {
    this.initTableData()
  }
}
</script>
<style scoped>

</style>