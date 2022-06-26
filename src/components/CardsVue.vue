<template>
  <div>
    <div class="row" style="margin:0px ;">
      <div class="col-xl-12">
        <section>
          <CardITem
            v-for="(item, index) in listofdata"
            v-bind:key="index"
            :header="item.head"
            :src="item.source"
            :txt="item.txt"
          ></CardITem>
        </section>
      </div>
    </div>

    <div class="row" style="margin:0px;">
    <div class="col-xl-12">
      <article>
        <div class="col-xl-5 buytheme">BUY THEME</div>
        <div class="col-xl-2 or"> OR </div>
        <div class="col-xl-5 viewdemo">VIEW DEMO</div>
      </article>
    </div>
    </div>
  </div>
</template>

<script>
import CardITem from "./CardITem.vue";
export default {
  name: "CardsVue",
  components: { CardITem },
  data() {
    return {
      listofdata: [
        {
          head: "CREATIVITY DESIGN",
          txt: "Interactive Animations Media Menagment Quality Assurance E-Commerce Solutions Community Management",
          source: require("@/assets/bulb.png"),
        },
        {
          head: "STRATEGY DESIGN",
          txt: "Interactive Animations Media Menagment Quality Assurance E-Commerce Solutions Community Management",
          source: require("@/assets/pen.png"),
        },
        {
          head: "ANALYTICS & REPORTING",
          txt: "Interactive Animations Media Menagment Quality Assurance E-Commerce Solutions Community Management",
          source: require("@/assets/params.png"),
        },
        {
          head: "BRAND EXPERIENCE",
          txt: "Interactive Animations Media Menagment Quality Assurance E-Commerce Solutions Community Management",
          source: require("@/assets/lab.png"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.col-xl-12{
  display: flex;
  justify-content: center;
  section {
  width: 90%;
  display: flex;
  justify-content: space-evenly;
  margin-top: 100px;
  margin-bottom: 100px;
}
article{
  width: 30%;
  display: flex;
  justify-content: center;
  font-size: 14px;
  color: white;
  position: relative;
  .buytheme{
    background-color: #444444;
    padding: 15px;
    padding-right: 20px;
  }
  .or{
            position: absolute;
    background-color: black;
    border-radius: 50px;
    /* height: 50px; */
    bottom: 11%;
    /* top: 15px; */
    /* font-size: 10px; */
    width: 10%;
    height: 77%;
    display: flex;
    align-items: center;
    justify-content: center;
    
  }
  .viewdemo{
  
    background-color: #5CC8C5;
    padding: 15px;
    padding-right: 20px;
  }
}
}

</style>
