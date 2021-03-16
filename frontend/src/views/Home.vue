<template>
  <div class="home">

      <div class="firstblock">
        <navbar></navbar>
        <div class="purpleTextImage">
          <div class="purple__text">
            <PurpleEyeText class="PT" ></PurpleEyeText>
          </div>
          <div class="eyeimg">
            <img class="PL" src="../assets/eyelogo2.svg" alt="">
          </div>
        </div>
      </div>

    <div class="secondblock">
      <TwoPanel class="twoelements"></TwoPanel>
    </div>
    <div class="threeblock">


      <div class="firstSite">
        <div class="firstSite__text">
            <h1>Site for Google</h1>
            <p>Это одна из первых наших работ</p>
        </div>
        <div class="firstSite__image">
          <ThreePanel class="image__one"></ThreePanel>
        </div>
      </div>


      <div class="secondSite">
        <div class="secondSite__image">
          <ThreePanelTwo class="image__one"></ThreePanelTwo>
        </div>
        <div class="secondSite__text">
          <h1>Site for Yandex</h1>
          <p>Это уже наш второй проект</p>
        </div>
      </div>


      <div class="thirdSite">
        <div class="thirdSite__image">
          <ThreePanelThree class="image__one"></ThreePanelThree>
        </div>
        <div class="thirdSite__text">
          <h1>Site for Yandex</h1>
          <p>Это уже наш второй проект</p>
        </div>
      </div>


    </div>
    <div class="fourBlock">
      <PeopleOne></PeopleOne>
    </div>
  </div>
</template>


<style>
::-webkit-scrollbar {
  width: 0;
}

.firstSite{
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: space-around;
  align-items: center;
  position: absolute;
  width: 100%;
}
.firstSite__text{
  width:30%;
  margin-left: 12%;
  position: relative;
  text-align: left;
}
.firstSite__text h1{
  font-family: Impact;
  width: 15%;
}
.firstSite__image{
  width:70%;
  position: relative;
}
.image__one{
  position: relative;
  left: -15%;
  transform: scale(0.5);
}
.secondSite{
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: space-around;
  align-items: center;
  position: absolute;
  width: 100%;
  margin-top: 30%;
}
.secondSite__text{
  width:30%;
  margin-left: 5%;
  position: relative;
  text-align: left;
}
.secondSite__image{
  width:70%;
  position: relative;
}
.secondSite__text h1{
  font-family: Impact;
  width: 15%;
}

.thirdSite{
  display: flex;
  flex-direction: row-reverse;
  flex-wrap: nowrap;
  justify-content: space-around;
  align-items: center;
  position: absolute;
  width: 100%;
  margin-top: 60%;
}
.thirdSite__text{
  width:30%;
  margin-left: 12%;
  position: relative;
  text-align: left;
}
.thirdSite__image{
  width:70%;
  position: relative;
}
.thirdSite__text h1{
  font-family: Impact;
  width: 15%;
}
.purpleTextImage{
  width: 100%;
  height: 100%;
  position: fixed;
  left: 0;
  display: flex;
  overflow: auto;
  justify-content: center;
  align-items: center;
}
.purple__text{
  display: block;
  border: none;
  width: 100%;
  height: 100%;
}
.PT{
  margin-left: 20%;
  margin-top: 15%;
  transform: scale(1.2);
}
.eyeimg{
  display: block;
  border: none;
  width: 100%;
  height: 100%;
}
.PL{
  margin-left: 25%;
  margin-top: 9%;
  transform: scale(1.5);
}
.twoelements{
  height: 100vh;
}
.firstblock {
  background-color: #24253d;
  position: relative;
  background-position: center center;
  height: 100vh;
}
.secondblock{
  background-color: #7275a3;
  position: relative;
  background-position: center center;
  height: 100vh;
}
.threeblock{
  background-color: #7275a3;
  position: relative;
  background-position: center center;
  height: 200vh;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
}
.fourBlock{
  position: relative;
  height: 100vh;
  background-color: #24253d;
}
@media (max-width: 700px) {
  .secondblock{
    height: 110vh;
  }
  .PT{
    margin-top: -25%;
    transform: scale(1.1);
    margin-left: 5%;
  }
  .PL{
    margin-top: 15%;
    transform: scale(1.5);
  }
  .purpleTextImage{
    flex-direction: column-reverse;
    align-items: center;
    justify-content: center;
  }
  .purple__text{
    display: block;
    border: none;
  }
  .eyeimg{
    display: block;
    border: none;
  }
  .image__one{
    transform: scale(0.2);
  }

}

</style>


<script>
  import Navbar from "../components/navbar";
  import TwoPanel from "@/components/twoPanel";
  import PurpleEyeText from "@/components/purpleEyeText";
  import ThreePanel from "@/components/threePanel";
  import ThreePanelTwo from "@/components/threePanelTwo";
  import ThreePanelThree from "@/components/threePanelThree";
  import PeopleOne from "@/components/peopleOne";

  export default {
    name: 'Home',
    components: {
      PeopleOne,
      ThreePanel,
      PurpleEyeText,
      TwoPanel,
      Navbar,
      ThreePanelTwo,
      ThreePanelThree
    },
    mounted() {

    }
  }
</script>
