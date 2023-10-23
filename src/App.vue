<template>
  <div class="container">
    <Input @post="addPost"/>
    <div class="items">
      <Item v-for="item in items" :item="item"/>
    </div>
  </div>
</template>

<script>
import Item from './components/Item'
import Input from './components/Input'
export default {
  components: {
    Item, Input
  },
  data() {
    return {
      items: [
        {
          title: 'Food',
          price: '100'
        },
        {
          title: 'lorem',
          price: '200'
        },
      ]
    }
  },
  methods: {
    addPost(post) {
      this.items.unshift(post)
    }
  }
}
</script>

<style scoped>

</style>