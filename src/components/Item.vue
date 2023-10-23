<template>
  <div class="item">
    <div class="item-title" v-text="item.title"></div>
    <div class="item-price" v-text="item.price"></div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

</style>