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
@import '@/assets/styles/compnonets/CardsVue.scss'

</style>
