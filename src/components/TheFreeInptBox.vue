<template>
  <div>
    <div class="things"><label for="inputThing">紀事</label></div>
    <input
      name="thingsText"
      id="inputThing"
      type="text"
      @change="handleOnChangeInput"
      :style="{ width: '100%' }"
    />
  </div>
</template>

<script>
export default {
  props: {
    thingsText: {
      required: true
    },
    handleInput: {
      required: true
    }
  },
  methods: {
    handleOnChangeInput(event) {
      this.handleInput(event)
    }
  }
}
</script>

<style scoped></style>
