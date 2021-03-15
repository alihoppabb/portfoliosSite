<template>
  <div class="home">
      <div class="firstblock">
        <navbar></navbar>
        <div class="purpleTextImage">
          <div class="purple__text">
            <PurpleEyeText class="PT" ></PurpleEyeText>
          </div>
          <div class="eyeimg">
            <img class="PL" src="../assets/eyelogo1.svg" alt="">
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
  margin-left: 5%;
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
.purpleTextImage{
  width: 100%;
  height: 100%;
  position: fixed;
  top: 15%;
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
  margin-top: 10%;
  transform: scale(1.2);
}
.eyeimg{
  display: block;
  border: none;
  width: 100%;
  height: 100%;
}
.PL{
  margin-left: 45%;
  margin-top: 5%;
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
  height: 500vh;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
}
@media (max-width: 700px) {
  .PT{
    margin: auto;
    transform: scale(0.8);
  }
  .PL{
    margin: auto;
    transform: scale(1);
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

  export default {
    name: 'Home',
    components: {
      ThreePanel,
      PurpleEyeText,
      TwoPanel,
      Navbar,
      ThreePanelTwo
    },
    mounted() {

    }
  }
</script>
