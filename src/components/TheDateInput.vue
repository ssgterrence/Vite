<template>
  <div>
    <div class="things"><label for="inputThing">日期</label></div>
    <input
      name="dateTime"
      id="inputThing"
      type="date"
      @change="handleOnChangeInput"
      :style="{ width: '100%' }"
    />
  </div>
</template>
<script>
export default {
  props: {
    dateTime: {
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
<style></style>
