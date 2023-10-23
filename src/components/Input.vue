<template>
  <form @submit.prevent="createNewPost">
    <input type="text" v-model="title" placeholder="something" required>
    <input type="text" v-model="price" placeholder="price" required>
    <button type="submit">search</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      title: '',
      price: ''
    }
  },
  methods: {
    createNewPost() {
      this.$emit('post', {
        title: this.title,
        price: this.price
      })
      this.title = ''
      this.price = ''
    }
  }
}
</script>

<style scoped>

</style>