<template>
  <div class="gridContainer">
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
    <div class="middleContent"></div>
    <div class="rightContent">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis maxime corporis explicabo ipsa
      ab dolorem veniam enim assumenda, quos magni nesciunt nemo ea sit error rerum sequi
      exercitationem hic delectus?
    </div>
  </div>
</template>
<script>
import TheNavigationBar from './TheNavigationBar.vue'
import TheTimesHeader from './TheTimesHeader.vue'
import TheLeftTextContent from './TheLeftTextContent.vue'
export default {
  components: {
    TheNavigationBar,
    TheTimesHeader,
    TheLeftTextContent
  }
}
</script>
<style scoped>
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
