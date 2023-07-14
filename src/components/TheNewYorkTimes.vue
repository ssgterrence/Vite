<template>
  <div class="gridContainer">
    <div class="header">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Non atque aspernatur impedit quasi
      quidem, mollitia officiis iure, accusantium, facilis consequuntur iste magni eius numquam.
      Quasi at doloremque, nostrum consequuntur totam sequi velit asperiores nam quam quaerat et
      recusandae sed provident aliquam tempora, impedit neque vel magnam nobis sunt dolor
      exercitationem facilis nemo error. Explicabo, architecto? Vel, non. Obcaecati, iure blanditiis
      incidunt impedit, fuga quam explicabo optio nihil mollitia aliquid at, soluta dolores
      deleniti. Nemo ad quo earum maiores dolorem, odit harum in aliquam, laborum possimus quasi at!
      Quas temporibus beatae veniam corrupti inventore esse mollitia, dolorem incidunt praesentium
      velit earum, dignissimos tempora debitis nemo consectetur doloribus provident tenetur!
      Suscipit laudantium ipsa nemo animi quasi dicta fugiat temporibus, ex ipsum quam corporis
      harum, nisi nam inventore. Dicta quaerat repudiandae odit at hic repellendus natus maiores
      amet? Molestias a eum earum minus necessitatibus cumque dolore odit! Blanditiis harum vel
      natus error sit laborum esse, corporis corrupti, ipsa voluptatibus iure obcaecati! Eaque
      praesentium quae, pariatur quisquam possimus provident dicta quia ea natus fugit ratione
      fugiat eum quod error aliquam, incidunt ex voluptas suscipit amet? Voluptate labore voluptates
      alias molestiae repellendus facere veritatis culpa eligendi temporibus aliquam? Eius itaque,
      impedit nisi aperiam nulla obcaecati.
    </div>
    <div class="navigationBar">
      LoremipsumdolorsitametconsecteturadipisicingelitMolestiasaperiamducimusquiaLoremipsumdolorsitametconsecteturadipisicingelitMolestiasaperia
    </div>
    <div class="hamburger">
      <div></div>
      <div></div>
      <div></div>
    </div>
    <div class="leftContent">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Maiores, dolores! Sed facere aliquam
      nobis, vel natus excepturi exercitationem eaque eum mollitia quod laborum, maxime laboriosam,
      praesentium animi nam! Perferendis, saepe?
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
export default {}
</script>
<style>
.gridContainer {
  gap: 10px;
  display: grid;
  margin-left: 100px;
  margin-right: 100px;
  grid-template-columns: repeat(12, 1fr);
}
.header {
  grid-column: span 12;
  background-color: aqua;
}

.navigationBar {
  grid-column: span 12;
  background-color: forestgreen;
}
.leftContent {
  grid-column: span 3;
  background-color: antiquewhite;
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
