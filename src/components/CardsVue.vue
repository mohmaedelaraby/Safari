<template>
    <div>
        <div class="row">
            <div class="col-xl-12">
                 <section>
                <CardITem v-for="(item,index) in 4" v-bind:key="index" ></CardITem>
            </section>
            </div>
           
        </div>
    </div>
</template>

<script>
import CardITem from './CardITem.vue';
    export default {
        name:"CardsVue",
    components: { CardITem }
}
</script>

<style lang="scss" scoped>
section{
    width: 100%;
    display: flex;
    justify-content: space-evenly;

    padding-top: 100px;
    padding-bottom: 100px;
}

</style>