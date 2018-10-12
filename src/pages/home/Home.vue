<template>
    <div>
        <home-header></home-header>
        <home-h-swiper></home-h-swiper>
    </div>
</template>

<script>
import HomeHeader from './components/Head'
import HomeHSwiper from './components/Swiper'
export default {
    name:'Home',
    components:{
        HomeHeader,
        HomeHSwiper
    }
}
</script>

<style scoped>

</style>

