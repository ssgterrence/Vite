<template>
  <div class="textInputContainer">
    <div><label for="inputBox">Input Box</label></div>
    <input id="inputBox" type="text" @input="handleTextInput" />
    <div>{{ text }}</div>
  </div>
</template>
<script>
export default {
  data: () => ({
    text: ''
  }),
  computed: {},
  methods: {
    handleTextInput(event) {
      this.text = event.target.value
    }
  }
}
</script>
<style>
.textInputContainer {
  text-align: center;
}
</style>
