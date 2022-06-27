<template>
  <div class="card">
    
    <div class="card__container">
      <div class="card__upper">
        <h2>THEME FOR CREATIVES & DOING THEME BUSINESS NOW</h2>
      </div>

      <div class="card__lower">
        <p class="card__txt">for Themeforest
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
    props:['header','txt']
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  background:linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.2)), url("@/assets/bg.png");
  .card__container {
    width: 80%;
    display: flex;
    flex-direction: column;
    padding: 50px;
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
      .card__btns {
       display: flex;
       align-items: center;
       justify-content: space-between;
       width: 24%;
       .btn{
        width: 48%;
        border-radius: 5px;
       }
       .btn-primary{
        background-color: #5CC8C5;
        border: none;
       }
       .btn-outline-primary{
        color:#5CC8C5;
        border:1px solid #5CC8C5;

        &:hover{
            color: white;
            background-color: #5CC8C5;
        }
       }
      }
    }
  }
}
</style>
