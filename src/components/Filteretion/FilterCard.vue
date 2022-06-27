<template>
  <div class="card">
    <img class="card-img-top" :src="src" alt=" img" />
    <div class="card-body">
      <p class="card_header">{{ header }}</p>
      <p class="card-text">{{ txt }}</p>
    </div>
    <div class="card__layout">
      <p class="card_header">{{ header }}</p>
      <p class="card-text">{{ txt }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["src", "header", "txt"],
};
</script>

<style lang="scss" scoped>
.card {
  width: 20%;
  border-radius: 0px;
  border: none;
  position: relative;
  @media (max-width: 320px) {
        width: 100%;
      }
  .card-img-top {
    border-radius: 0px;
    img{
      margin: 0;
    }
  }
  .card_header {
    font-size: 15px;
    font-weight: 500;
    color: #444444;
    @media (max-width:770px) {
      font-size: 10px;
    }
  }
  .card-text {
    font-size: 13px;
    color: #444444;
     @media (max-width:770px) {
      font-size: 8px;
    }
  }
  .card__layout {
    position: absolute;
    
    width: 100%;
    height: 100%;
    opacity: 0;
    cursor: pointer;
    background: rgba(92, 200, 197, 0.9);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    .card_header {
      font-size: 15px;
      font-weight: 500;
      color: white;
    }
    .card-text {
      font-size: 13px;
      color: white;
    }

    &:hover {
      opacity: 1;
    }
  }
}
</style>
