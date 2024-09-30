<template>
  <div v-if="item.isVisible">
    <h3>{{ item.name }}</h3>
    <p>Price: {{ item.price }}</p>
    <button @click="addToCart">Add to Cart</button>
  </div>
</template>

<script>
export default {
  name: 'Item',
  props: {
    item: {
      type: Object,
      required: true
    }
  },
  methods: {
    addToCart() {
      console.log(`Item added to cart: Name: ${this.item.name}, Price: ${this.item.price}`)
      this.$emit('add-to-cart', this.item)
    }
  }
}
</script>
<style scoped>
div {
  border: 2px solid gainsboro;
  padding: 11px;
  text-align: center;
  border-radius: 11px;
  margin-bottom: 6px;
}
button{
  border: none;
  background: none;
  padding: 10px;
  background-color: aqua;
  color: white;
  border-radius: pointer;
  font-weight: bold;
}
button:hover{
  background-color: darkred;
  
}
</style>