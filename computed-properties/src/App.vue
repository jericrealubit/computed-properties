<template>
  <h2>Firstname: {{ firstName }}</h2>
  <h2>Lastname: {{ lastName }}</h2>
  <h2>Fullname: {{ fullName }}</h2>
  <h2>
    Total: {{ total }}
  </h2>
</template>

<script>
  export default {
    data() {
      return {
        firstName: 'John',
        lastName: 'Doe',
        items: [
          {
            id: 1,
            title: 'TV',
            price: 100
          },
          {
            id: 2,
            title: 'Phone',
            price: 200
          },
          {
            id: 3,
            title: 'Laptop',
            price: 300
          }
        ]
      }
    },
    computed: {
      fullName() {
        return `${this.firstName} ${this.lastName}`
      },
      total() {
        return this.items.reduce((total, curr) => (total = total + curr.price), 0)
      }
    }
  }
</script>




<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

