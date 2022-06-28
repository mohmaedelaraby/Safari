<template>
  <div class="card">
    <div class="card-img-top">
      <div class="cirlce">
        <img :src="src" alt="pen" />
      </div>
    </div>
    <div class="card-body">
      <p class="cardheader">{{ header }}</p>
      <p class="card-text">{{ txt }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardITem",
  props: ["header", "txt", "src"],
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/compnonets/CardITem.scss'
</style>
