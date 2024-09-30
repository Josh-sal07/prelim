<template>
  <div>
    <AppItem
      v-for="item in filteredItems"
      :key="item.id"
      :item="item"
      @add-to-cart="handleAddToCart"
    />
  </div>
</template>

<script>
import AppItem from './AppItem.vue'

export default {
  name: 'Itemlist',
  components: {
    AppItem
  },
  props: {
    items: {
      type: Array,
      required: true
    }
  },
  computed: {
    filteredItems() {
      return this.items.filter((item) => item.isVisible)
    }
  },
  methods: {
    handleAddToCart(item) {
      console.log(`Item added to cart: Name: ${item.name}, Price: ${item.price}`)
    }
  }
}
</script>

<style scoped>

</style>