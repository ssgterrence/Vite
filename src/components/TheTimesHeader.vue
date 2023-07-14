<template>
  <div class="HeaderContainer">
    <div class="topestContainer">
      <div class="leftICon">
        <div class="hamburger">
          <div></div>
          <div></div>
          <div></div>
        </div>

        <div class="searchSign"><font-awesome-icon icon="search" /></div>
      </div>
      <div class="middelTopestCountryAndLanguage">
        <div class="usa">U.S</div>
        <div class="international">INTERNATIONAL</div>
        <div class="canada">CANADA</div>
        <div class="espanol">ESPANOL</div>
        <div class="chinese">中文</div>
      </div>
      <div class="rightICOn">
        <div class="subscribeFor">SUBSCRIBE FOR $0.5/WEEK</div>
        <div class="login">LOGIN</div>
      </div>
    </div>
    <!--  -->
    <div class="bottomPart">
      <div class="leftText">
        <div class="JulyThursday">Thursday, July 13, 2023</div>
        <div class="todayPaper">Todady's Paper</div>
      </div>
      <div class="TheNewYorksTimeImage">
        <img src="New-York-Times-Logo8x6_0.jpg" alt="TheNewYorksTimeImage" class="custom_image" />
      </div>
      <div class="dateTimeMediaQuery">
        <div class="dataTimeLine"></div>
        <div class="innerContentMediaQuery">
          <div class="dataContentMediaQuery">Friday, July 14, 2023</div>
          <div class="subscriberMediaQuery">SUBSCRIBE FOR $0.50/WEEK</div>
        </div>
        <div></div>
      </div>
      <div class="rightText">
        <div class="sp500">S&P 500</div>
        <div class="percentage">+0.14%</div>
      </div>
    </div>
  </div>
</template>
<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { library } from '@fortawesome/fontawesome-svg-core'
import { faSearch } from '@fortawesome/free-solid-svg-icons'
library.add(faSearch)
export default {
  components: {
    FontAwesomeIcon
  }
}
</script>
<style scoped>
.HeaderContainer {
  margin-top: 4px;
}
.topestContainer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.leftICon {
  display: flex;
}
.leftICon > div {
  /* margin: 0 4px; */
}
.searchSign {
  margin-left: 1rem;
}

.middelTopestCountryAndLanguage {
  margin-left: 7rem;
  font-size: 12px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  display: flex;
}
.middelTopestCountryAndLanguage > div {
  margin: 0 4px;
}
.international {
  font-weight: bold;
}

.rightICOn {
  display: flex;
  font-size: 14px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  color: white;
}

.rightICOn > div {
  margin: 0 4px;
}
.subscribeFor {
  background-color: rgb(69, 122, 160);
  padding: 3px;
  border-radius: 4px;
}
.login {
  background-color: rgb(69, 122, 160);
  padding: 2px;
  border-radius: 4px;
}

.hamburger div {
  width: 25px;
  height: 2px;
  background-color: #333;
  margin: 3px 0;
}

.bottomPart {
  display: flex;
  justify-content: space-between;
}
.leftText {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.TheNewYorksTimeImage {
  width: auto;
  height: 100px;
}

.JulyThursday {
  font-weight: bold;
}
.rightText {
  display: flex;
  align-items: center;
}
.percentage {
  color: rgba(165, 200, 164);
  margin-left: 0.5rem;
}
.dateTimeMediaQuery {
  display: none;
}

@media screen and (max-width: 1300px) {
  .TheNewYorksTimeImage {
    display: none;
  }
  .leftText {
    display: none;
  }
  .rightText {
    display: none;
  }
  .dateTimeMediaQuery {
    display: block;
    width: 100%;
  }

  .innerContentMediaQuery {
    margin: 1rem 0;
    display: flex;
    flex-grow: auto;
    justify-content: flex-end;
  }
  .subscriberMediaQuery {
    margin-left: 15rem;
    color: rgba(90, 162, 132);
  }

  .dataTimeLine {
    margin-top: 0.5rem;
    border-bottom: 1px solid rgba(226, 226, 226);
  }
  .dateTimeMediaQuery:nth-child(3) {
    margin-top: 0.5rem;
    border-bottom: 1px solid rgba(226, 226, 226);
  }
}
@media screen and (max-width: 1008px) {
  .searchSign {
    display: none;
  }
  .middelTopestCountryAndLanguage {
    display: none;
  }
  .rightText {
    display: none;
  }
}
</style>
