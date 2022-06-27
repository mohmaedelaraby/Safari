<template>
  <div class="card">
    <div class="card__container">
      <div class="card__upper">
        <h2>{{header}}</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit aliquam</p>
      </div>

      <div class="card__lower">
        <p class="card__txt">{{txt}}
        </p>
        <p class="card__signture">Morton Reder <strong>Co-Founder</strong></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props:['header','txt']
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  justify-content: center;
  align-items: center;
  color: #222222;
  .card__container {
    width: 80%;
    display: flex;
    flex-direction: column;
    .card__upper {
      margin-top: 100px;
      margin-bottom: 55px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      h2 {
        margin-bottom: 50px;
        font-weight: 600;
      }
      p {
        width: 80%;
      }
    }
    .card__lower {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      margin-bottom: 50px;
      .card__txt {
        font-size: 16px;
        line-height: 1.6;
        width: 70%;
        font-style: italic;
      }
      .card__signture {
        font-size: 16px;
        strong {
          color: #88888888;
        }
      }
    }
  }
}
</style>
