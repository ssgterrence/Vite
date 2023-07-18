<script>
export default {}
</script>
<template>
  <div class="girlStandContainer">
    <div><img class="girlsImage" src="girlsStand.jpg" /></div>
    <div class="textContainer">
      <h3 class="heading">Want to Save the Castle? Start a Podcast.</h3>
      <div class="content">
        The Duchess of Rutland learned the art of running a castle on the job. Then she started
        interviewing other duchesses on how they make it work.
      </div>
    </div>
  </div>
  <!--  -->
  <div class="twoImageStore">
    <div class="animalContainer">
      <img class="animal" src="animal.jpg" />
      <h5>She steals surfboards by the seashore. She’s a sea otter.</h5>
      <div>5 MIN READ</div>
    </div>
    <div class="line"></div>
    <div class="vegsContainer">
      <img class="vegesImg" src="veges.jpg" />
      <h5>Is it a meal? A snack? No, it’s “girl dinner.”</h5>
      <div>5 MIN READ</div>
    </div>
  </div>
</template>

<style>
.girlStandContainer::after {
  content: '';
  display: block;
  width: 100%;
  height: 1px;
  background-color: #000;
  margin-top: 10px;
  margin-bottom: 20px;
}

.twoImageStore {
  display: flex;
  justify-content: space-between;
}

.girlsImage {
  max-width: 100%;
}
.animalContainer {
  width: 45%;
}

.animalContainer > div:nth-child(3) {
  color: aqua;
}
.vegsContainer > div:nth-child(3) {
  color: aqua;
}

.line {
  border-left: 1px solid gray;
}
.animal {
  max-width: 100%;
}
.vegesImg {
  max-width: 100%;
}
.vegsContainer {
  width: 45%;
}
</style>
