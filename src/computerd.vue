<template>
  <div>
    <h1>Total Price: ${{ totalPrice }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { name: 'Laptop', price: 1000 },
        { name: 'Phone', price: 500 },
        { name: 'Tablet', price: 300 }
      ]
    };
  },
  computed: {
    totalPrice() {
      return this.items.reduce((sum, item) => sum + item.price, 0);
    }
  }
};
</script>

 items: [
        { name: 'Iphone', price: 1000 },
        { name: 'Samsung', price: 500 },
        { name: 'Mega 1', price: 300 }
      ]