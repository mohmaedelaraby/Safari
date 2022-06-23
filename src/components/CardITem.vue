<template>
  <div class="card">
    <div class="card-img-top" >
        <div class="cirlce">
            <img src="@/assets/pen.png" alt="pen"/>
        </div>
    </div>
    <div class="card-body">
     <p class="cardheader">STRATEGY DESIGN</p>
      <p class="card-text">
        Some quick example text to build on the card title and make up the bulk
        of the card's content.
      </p>
    </div>
  </div>
</template>

<script>

export default {
    name: "CardITem",
};
</script>

<style lang="scss" scoped>
.card{
    width: 270px;
    height: 410px;
    border: none;
    border-radius: 0px;
    display: flex;
    align-items: center;
    justify-content: center; 
    transition: 0.4s ease-in;

    &:hover{
        border: 1px solid gray;
         transition: 0.4s ease-in;
    }
    .card-img-top{
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 30px;
.cirlce{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 110px;
    height: 110px;
    border-radius: 50%;
    cursor: pointer;
     background-color: rgb(233, 232, 232);
     transition: 0.4s ease-in;
     &:hover{
        background-color: #5CC8C5;
         transition: 0.4s ease-in;
     }
}
}
.card-body{

    flex-direction: column;
    display: flex;
    align-items: center;
    justify-content: center;
    .cardheader{
        font-weight: 500;
        font-size: 15px;
        
    }
    .card-text{
        width: 50%;
        line-height: 2;
        font-size: 13px;
    }
}
}


</style>
