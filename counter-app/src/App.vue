<template>
  <div class="counter-app">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">Counter App</a>
    </nav>
    <div class="container mt-4">
      <h1 class="text-center">Counter Application</h1>
      <div class="text-center">
        <p>Count: {{ count }}</p>
        <button class="btn btn-primary" @click="increment">Increment</button>
        <button class="btn btn-danger" @click="decrement">Decrement</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      count: 0
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      if (this.count > 0) {
        this.count--;
      }
    }
  }
};
</script>

<style>
@import 'bootstrap/dist/css/bootstrap.css';

.counter-app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}

.container {
  padding: 20px;
}
</style>
