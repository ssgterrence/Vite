<script>
// import TheNavigationBar from './TheNavigationBar.vue'
// import TheTimesHeader from './TheTimesHeader.vue'
// import TheLeftTextContent from './TheLeftTextContent.vue'
// import TheRightContent from './TheRightContent.vue'
// import TheMiddleImage from './TheMiddleImage.vue'
export default {
  components: {
    // TheNavigationBar,
    // TheTimesHeader,
    // TheLeftTextContent,
    // TheRightContent,
    // TheMiddleImage
  },
  data: () => ({
    formattedMessage: '<strong>Hello</strong> <em>Vue.js</em>'
  })
}
</script>
<template>
  <!-- <div class="gridContainer">
    <div class="header"><TheTimesHeader /></div>
    <div class="navigationBar"><TheNavigationBar /></div>
    <div class="hamburger">
      <div></div>
      <div></div>
      <div></div>
    </div>
    <div class="leftContent">
      <TheLeftTextContent />
    </div>
    <div class="middleContent">
      <TheMiddleImage />
    </div>

    <div class="rightContent">
      <TheRightContent />
    </div>
  </div> -->
  <div v-html="formattedMessage"></div>
  <div class="grid">
    <div class="left">Cupcakes lor</div>
    <div class="right">
      Muffins Lorem ipsum dolor, sit amet consectetur adipisicing elit. Qui delectus labore debitis
      assumenda dolore voluptas maiores magni sint, laudantium enim, quos autem, dolorum quisquam
      inventore! Nobis temporibus consequuntur quod accusantium!
    </div>
  </div>
</template>

<style scoped>
.grid {
  display: grid;
  height: 50vh;
  grid-template-columns: 1fr 1fr;
  transition: 500ms;
  gap: 2px;
}
.left {
  background-color: bisque;
}

/*  */
.gridContainer {
  gap: 10px;
  display: grid;
  margin-left: 100px;
  margin-right: 100px;
  grid-template-columns: repeat(12, 1fr);
}
.header {
  grid-column: span 12;
}
.navigationBar {
  grid-column: span 12;
}
.leftContent {
  grid-column: span 3;
}
.middleContent {
  grid-column: -10/-4;
  background-color: goldenrod;
}
.rightContent {
  grid-column: -4/-1;
  background-color: darkcyan;
}
.hamburger {
  display: none;
  cursor: pointer;
}
.hamburger div {
  width: 25px;
  height: 2px;
  background-color: #333;
  margin: 3px 0;
}
@media screen and (max-width: 1348px) {
  .navigationBar {
    display: none;
  }
  .hamburger {
    display: grid;
    grid-column: span 12;
  }
}
@media screen and (max-width: 999px) {
  .leftContent {
    grid-column: span 5;
  }
  .middleContent {
    grid-column: -8/-1;
  }
  .rightContent {
    grid-column: span 12; /* spans across all columns */
    background-color: darkcyan;
  }
}
</style>
