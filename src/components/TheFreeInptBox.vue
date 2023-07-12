<template>
  <div>
    <div class="things"><label for="inputThing">紀事</label></div>
    <input
      name="thingsText"
      id="inputThing"
      type="text"
      @change="handleEmitHInput"
      :style="{ width: '100%' }"
    />
  </div>
</template>

<script>
export default {
  data: () => ({
    thingsText: ''
  }),
  emit: ['handle-input'],
  methods: {
    handleEmitHInput(event) {
      this.$emit('handle-input', event)
    }
  }
}
</script>

<style scoped></style>
