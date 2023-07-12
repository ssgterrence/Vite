<template>
  <div class="Counter_container">
    <h1>{{ count }}</h1>
    <button class="incrementBtn" @click="increment">Click me To + the Count</button>
    <button class="decrementBtn" @click="decrement">Click me To - the Count</button>
    <p v-if="count >= 10" class="successMessage">Successful</p>
    <p v-else class="failMessage">Fail</p>
  </div>
  <section>
    <div>{{ parentCount }}</div>
    <button class="parentIncrement" @click="parentIncrement">
      Click parentIncrement the Count
    </button>
  </section>
</template>

<script>
export default {
  props: {
    parentCount: {
      required: true,
      default: 50
    },
    parentIncrement: {
      required: true
    }
  },
  data: () => {
    return { count: 0 }
  },
  methods: {
    increment() {
      return this.count++
    },
    decrement() {
      return this.count--
    }
  }
}
</script>

<style scoped>
.Counter_container {
  text-align: center;
}
.incrementBtn {
  background-color: palevioletred;
}
.decrementBtn {
  background-color: gold;
}
.successMessage {
  color: green;
}
.failMessage {
  color: red;
}
.parentIncrement {
  background-color: aqua;
}
</style>
