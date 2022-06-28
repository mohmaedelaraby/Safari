<template>
  <div class="card">
    
    <div class="card__container">
      <div class="card__upper">
        <h2>THEME FOR CREATIVES & DOING THEME BUSINESS NOW</h2>
      </div>

      <div class="card__lower">
        <p class="card__txt">for {{txt}}
        </p>
        <div class="card__btns">
            <button type="button" class="btn btn-primary">Live Demo</button>
            <button type="button" class="btn btn-outline-primary">View Work</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props:['txt']
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/compnonets/BannerCart.scss'
</style>
