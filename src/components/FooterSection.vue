<template>
  <section>
    <div class="row">
      <div class="header">
        <div class="header__slogn">
          <p>We Are Hiring A Creative Web Designer</p>
          <img src="@/assets/arrow.svg" alt="arrow" />
        </div>
      </div>
    </div>
    <div class="row" style="background-color: #222222">
      <div class="container">
        <div class="row">
          <div class="col-xl-3 col-sm-6 col-12">
            <div class="footer__upper">
              <h3>STAY IN TOUCH</h3>
              <p>
                Nunc a urna sed neque fermentum pharetra. Aliquam suscipit purus
                nisi convallis nulla.
              </p>
              <img src="@/assets/flednr.svg" alt="flender" />
            </div>
            <div class="footer__lower">
              <div class="col-xl-6 col-sm-6 col-xs-12">
                <h4 class="footer__lower__header">LOCATION</h4>
                <p class="footer__lower__txt">
                  4456 Bee Street Hoxeyville, MI 49641
                </p>
              </div>
              <div class="col-xl-6 col-sm-6 col-xs-12">
                <h4 class="footer__lower__header">LOCATION</h4>
                <p class="footer__lower__txt">
                  4456 Bee Street Hoxeyville, MI 49641
                </p>
              </div>
            </div>
          </div>

          <div class="col-xl-3 col-sm-6 col-12">
            <div class="footer__upper">
              <h3>FLICKR FEED</h3>
            </div>
            <div class="footer__lower">
              <div class="img__container">
                <img
                  v-for="(item, index) in footerIMG"
                  v-bind:key="index"
                  :src="item"
                  alt="footerimg"
                />
              </div>
            </div>
          </div>

          <div class="col-xl-3 col-sm-6 col-12">
            <div class="footer__upper">
              <h3>TWEETS</h3>
            </div>
            <div class="footer__lower">
              <div class="L">
                <div v-for="item in 3" v-bind:key="item" class="L__container">
                  <img src="@/assets/L.svg" alt="L" />
                  <p>
                    Nunc a urna sed neque ferment pharetra. purus nisi convallis
                    nulla <strong>2 days ago </strong>
                  </p>
                </div>
              </div>
            </div>
          </div>

          <div class="col-xl-3 col-sm-6 col-xs-12">
            <div class="row">
              <ul>
                <li v-for="item in 6" v-bind:key="item">
                  <div class="list-item">
                    <div class="list-item-arrow">
                      <img src="@/assets/Shape6.svg" alt="x" />
                    </div>
                    <div class="list-item-txt">Theme</div>
                  </div>
                  <hr />
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="row" style="background-color: #222222">
     
        <div class="last_footer">
            <div class="left_footer_container">
                    <div class="left">2013 © Unify. ALL Rights Reserved.</div>
            <div class="right">Designed by PsdBooster</div>
            </div>
        
        </div>

    </div>
  </section>
</template>

<script>
const img = require("@/assets/footer.jpg");
export default {
  data() {
    return {
      footerIMG: [img, img, img, img, img, img, img, img, img, img, img, img],
    };
  },
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/compnonets/Footer.scss'
</style>
