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
@import '@/assets/styles/compnonets/TestMoneliesCart.scss'
</style>
