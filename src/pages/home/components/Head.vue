<template>
    <div class="header">
        <div class="header_left">
            <p>左边</p>
        </div>
        <div class="header_input">
            <input type="text">
        </div>
        <div class="header_right">
            <p>右边</p>
        </div>
    </div>
</template>

<script>
export default {
    name:'HomeHeader'
}
</script>

<style scoped>
    .header{
        height: .88rem;
        background-color: red;
        display: flex;
    }
    .header_left{
        width: .6rem;
    }
    .header_right{
        width: .6rem;
    }
    .header_input{
       flex :1;
        background-color: aliceblue;
    }
    .header_input input{
        border-radius: 4px;
        margin-top: .2rem;
        border:none;
    }
</style>

