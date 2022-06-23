<template>
    <div class="banner_bg">
        <div class="banner_bg_contianer">
            <SwipperCompnent>
                LLLL
            </SwipperCompnent>
        </div>
    </div>
</template>

<script>
import SwipperCompnent from './SwipperCompnent.vue'
export default {
    data(){
        return{
            listOfData:["THEME FOR CREATIVES & DOING THEME BUSINESS NOW","DOING THEME BUSINESS NOW"]
        }
    },
    components: { SwipperCompnent }
} 
</script>

<style lang="scss" scoped>
.banner_bg{
    background: url("@/assets/bg.png");
    width: 100%;
    height: 80vh;
    display: flex;
    align-items: center;
    justify-content: center;
    .banner_bg_contianer{
        background-color: red;
        width: 90%;
        height: 90%;
        display: flex;
        align-items: center;
        justify-content: center;
    }
}

</style>