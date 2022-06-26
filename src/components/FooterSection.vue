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
    <div class="row" style="background-color: #222222;">
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

        <div class="col-xl-3 col-sm-6 col-12" style="margin-left: 15px">
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

        <div class="col-xl-3 col-sm-6 col-12" style="margin-left: 15px">
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
        <div class="col-xl-3 col-sm-6 col-xs-12"></div>
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
section {
  .row {
    margin: 0;
    .header {
      width: 100%;
      background-color: #52a7dd;
      display: flex;
      align-items: center;
      justify-content: center;
      padding-top: 20px;
      padding-bottom: 20px;
      .header__slogn {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 40%;

        p {
          color: white;
          font-size: 22px;
          margin-bottom: 0;
        }
      }
    }
    .container {
      width: 95%;
      margin-top: 95px;
      background: #222222;
      display: flex;
      margin-bottom: 95px;
      .footer__upper {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;

        h3 {
          font-size: 14px;
          font-weight: 600;
          margin-bottom: 20px;
          display: flex;
          color: white;
        }
        p {
          font-size: 13px;
          color: #888888;
          text-align: left;
        }

        img {
          width: 70%;
        }
      }
      .footer__lower {
        display: flex;
        margin-top: 25px;
        .footer__lower__header {
          font-size: 14px;
          font-weight: 600;
          display: flex;
          color: white;
        }
        .footer__lower__txt {
          font-size: 12px;
          color: #888888;
          text-align: left;
        }
        .img__container {
          display: flex;
          flex-wrap: wrap;
          width: 80%;
          align-items: center;
          justify-content: space-between;
        }

        .L{
            display: flex;
            flex-direction: column;
            .L__container{
          display: flex;
          align-content: center;
          justify-content: space-between;
          img{
                width: 10%;
    /* margin: 9px; */
    margin-right: 16px;
    /* display: flex; */
    height: 45%;
          }
            p {
              color: white;
              text-align: left;
            }
            strong {
              color: #888888;
            }
          
        }
        }
        
      }
    }
  }
}
</style>
