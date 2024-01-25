<template>
<div class="ava-wrap">
    <div class="top">
        <div class="ava">
            <img src="./../assets/avatar.jpg" alt="">
        </div>
        <div class="level">
            Новый уровень!
        </div>
    </div>
    <div class="bottom">
        <p>Активные эффекты</p>
        <div class="effects">
            <div class="item-effects border-gray"><p class="gray" >2</p></div>
            <div class="item-effects border-gray"><p class="gray" >2</p></div>
            <div class="item-effects border-green"><p class="green" >2</p></div>
            <div class="item-effects border-red"><p class="red" >2</p></div>
        </div>
    </div>
</div>
</template>

<script>
    export default {
        name: 'Ava'
    }
</script>

<style scoped>
.item-effects{
    height: 30px;
    width: 30px;
    background-color: #211a14;
    background-image: url("./../assets/coin.png");
    background-size: contain; 
    /* border: #796857 1px solid; */
    border-radius: 4px;
    display: flex;
    position: relative;
}
.border-red{
    border: #bc122e 1px solid;
}
.border-green{
    border: #15a14b 1px solid;
}
.border-gray{
    border: #5f5f5f 1px solid;
}
.red{
    background-color: #bc122e;
}
.green{
    background-color: #15a14b;
}
.gray{
    background-color: #5f5f5f;
}
.item-effects p{
position: absolute;
height: 12px;
width: 12px;
font-size: 10px;
display: flex;
align-items: center;
justify-content: center;
color: #f1ebde;
bottom: 0;
right: 0;
}

.effects{
    margin-top: 12px;
    display: grid;
    grid-template: 1fr 1fr /1fr 1fr 1fr;
    gap: 6px; 
}
.bottom{
    min-height: 160px;
    margin-top: -10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    z-index: 0;
    background: linear-gradient(180deg, rgba(234, 200, 156, 0.663) -60%, rgba(33, 26, 20, 0.723) 20%, rgba(0,0,0,0) 100%);
}
.bottom > p{
margin-top: 30px;
font-size: 14px;
color: #c4baa7;
letter-spacing: 1px;;
}
.ava{
    border-bottom: 2px solid #796857;
    border-radius: 6px;
    
    height: 126px;
    overflow: hidden;
}
.level{
    width: 100%;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: .1em;
    color: #a68245;
}
.ava img{
height: 122%;

}
.top{
    position: relative;
    height: 150px;
    border: 2px solid #936f4b;
    border-radius: 6px;
    background-color: #211a14;
    z-index: 1;
}
</style>