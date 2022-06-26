<template>
  <div class="card">
    <div class="card-img-top" >
        <div class="cirlce">
            <img :src="src" alt="pen"/>
        </div>
    </div>
    <div class="card-body">
     <p class="cardheader"> {{header}}</p>
      <p class="card-text">{{txt}}
      </p>
    </div>
  </div>
</template>

<script>

export default {
    name: "CardITem",
    props:['header','txt','src']
};
</script>

<style lang="scss" scoped>
.card{
    width: 270px;
    border: none;
    border-radius: 0px;
    display: flex;
    align-items: center;
    justify-content: center; 
    border: 1px solid white;
    margin-left: 2px;

    &:hover{
        border: 1px solid gray;
    }
    .card-img-top{
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 30px;
    padding-bottom: 30px;
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
        width: 60%;
        line-height: 2;
        font-size: 13px;
    }
}
}


</style>
