<template>
    <div class="header-wrap">
        <div class="logo">
            GIANT'S VALE
        </div>
        <div class="player">
            <p>Player mode</p>
            <div class="username">
                Masha_203
                <img src="./../assets/triangle.svg" alt=""> 
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>
.player{
display: flex;
justify-content: space-between;
align-items: center;
width: 192px;
font-size: 12px;
margin-right: 60px;
letter-spacing: 1px;
color: #a68245;
}
.player img{
height: 12px;
margin-left: 2px;
}
.player p{
font-size: 10px;
border-right: 1px solid #5d5349;
padding-right: 12px;
height: 14px;
display: flex;
align-items: center;
letter-spacing: 2px;
color: #706450;
}
.logo{
    margin-left: 46px;
    font-size: 14px;
    font-weight: 500;
    letter-spacing: 0.43em;
    color: #a68245;
}
.header-wrap{
    height: 26px;
    width: inherit;
    background-color: rgb(37, 25, 9);
    display: flex;
    justify-content: space-between;
    align-items: center;
}
</style>