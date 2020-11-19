<template>
  <div>
    <a-form :from="form">
      <a-form-item v-for="item in formList" :key="item">
        <a-input v-decorator="[ item ]" />
      </a-form-item>
    </a-form>
  </div>
</template>

<script>
export default {
  name: 'form-com',
  data() {
    return {
      form: this.$form.createForm(this, { name: 'form' }),
      formList: []
    };
  },
  methods: {
    initForm() {
      const element = [];
      for (let index = 1; index < 100; index++) {
        element.push((1000 + index).toString())
      }
      this.formList.splice(0, this.formList.length, ...element)
    }
  },
  mounted() {
    this.initForm()
  }
}
</script>
<style scoped>

</style>