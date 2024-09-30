<template>
  <div>
    <ItemList :items="Items" />
  </div>
</template>

<script>
import ItemList from './components/ItemList.vue'

export default {
  name: 'App',
  components: {
    ItemList
  },
  data() {
    return {
      items: [
        { id: 1, name: 'Item 1', price: 10, isVisible: true },
        { id: 2, name: 'Item 2', price: 20, isVisible: false }
      ]
    }
  }
}
</script>

<style scoped></style>