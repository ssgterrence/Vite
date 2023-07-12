<template>
  <div>
    <div class="things"><label for="inputThing">時間</label></div>
    <input
      name="timeslot"
      id="inputThing"
      type="time"
      @change="handleOnChangeInput"
      :style="{ width: '100%' }"
    />
  </div>
</template>
<script>
export default {
  props: {
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
