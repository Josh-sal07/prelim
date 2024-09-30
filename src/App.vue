<template>
  <div>
    <Itemlist :items="items" />
  </div>
</template>

<script>
import Itemlist from './components/Itemlist.vue'

export default {
  name: 'App',
  components: {
    Itemlist
  },
  data() {
    return {
      items: [
        { id: 1, name: 'Item 1', price: 10, isVisible: true },
        { id: 2, name: 'Item 2', price: 20, isVisible: true },
        { id: 3, name: 'Item 3', price: 30, isVisible: true },
        { id: 4, name: 'Item 4', price: 40, isVisible: true },
        { id: 5, name: 'Item 5', price: 50, isVisible: true },
        { id: 6, name: 'Item 6', price: 60, isVisible: true },
        { id: 7, name: 'Item 7', price: 70, isVisible: true },
        { id: 8, name: 'Item 8', price: 80, isVisible: true },
      ]
    }
  }
}
</script>

<style scoped></style>