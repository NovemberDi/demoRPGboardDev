<template>
    <div class="storage-wrap">
        <div class="ower-top">
                <div>Способности</div>
                <div class="activ">Снаряжение</div>
                <div>Книга Заклинаний</div>
                <div>Локация</div>
            </div>
       <div class="main-block">
        
            <div class="main-block-item">
                <img src="./../assets/9.png" alt="">
            </div>
            <div class="main-block-item">
                <img src="./../assets/7.png" alt="">
            </div>
            <div class="main-block-item">
                <img src="./../assets/10.png" alt="">
            </div>
            <div class="main-block-item">
                <img src="./../assets/ring1.png" alt="">
            </div>
            <div class="main-block-item">
                <img src="./../assets/culon.png" alt="">
            </div>
            <div class="main-block-item">
                <img src="./../assets/ring2.png" alt="">
            </div>
            <div class="main-block-item">
                <img src="./../assets/8.png" alt="">
            </div>
            <div class="main-block-item">
                <img src="./../assets/1.png" alt="">
            </div>
            <div class="main-block-item">
                <img src="./../assets/5.png" alt="">
            </div>
       </div>
       <div class="right-block">
        <div class="right-block-item">
                <img src="./../assets/3.png" alt="">
            </div>
            <div class="right-block-item">
                <img src="./../assets/6.png" alt="">
            </div>
            <div class="right-block-item">
                <img src="./../assets/4.png" alt="">
            </div>
       </div>
       <div class="bottom-block">
            <div class="bottom-block-item"> </div>
            <div class="bottom-block-item"></div>
            <div class="bottom-block-item"><img src="./../assets/2.png" alt=""></div>
            <div class="bottom-block-item"></div>
            <div class="bottom-block-item"></div>
       </div>
    </div>
</template>

<script>
    export default {
        name: 'Storage'
    }
</script>

<style scoped>
.ower-top{
    display: flex;
    justify-content: center;
    align-items: center;
    /* margin-top: -2px; */
    color: #978e7e;
    position: absolute;
    top: 0;
    left: 50%;
    transform: translate(-50%, -12px);
    z-index: 5;
}
.ower-top div{
    border: 2px solid #936f4b;
    border-radius: 10px;
    background-color: #211a14;
    height: 16px;
    font-size: 12px;
    letter-spacing: 1px;
    margin: 0 10px;
    padding: 0 8px;
    width: max-content;
}
.activ{
    color: #ece8e1;
}


.bottom-block .bottom-block-item:nth-child(3){
    grid-area: 1/3/1/5;
    background: radial-gradient(  rgba(203, 162, 95, 0.683) -60%,  rgba(0,0,0,0) 90% );

}
.right-block .right-block-item:nth-child(1){
    grid-area: 1/1/4/1;
}
.right-block .right-block-item:nth-child(2){
    grid-area: 4/1/6/1;
}
.right-block .right-block-item:nth-child(3){
    grid-area: 6/1/8/1;
}
.right-block-item{
    position: relative;
    border: 3px solid #605440;
    border-radius: 6px;
    overflow: hidden;
    background: radial-gradient(  rgba(203, 162, 95, 0.683) -60%,  rgba(0,0,0,0) 90% );
}
.bottom-block-item{
    position: relative;
    border: 3px solid #605440;
    border-radius: 6px;
    height: 60px;
    min-width: 60px;
    overflow: hidden;
}
.right-block-item > img{
height: 100%;
}
.bottom-block-item > img{
height: 100%;
}
.main-block-item > img{
height: 100%;
}
.main-block-item{
    position: relative;
    border: 3px solid #605440;
    border-radius: 6px;
    overflow: hidden;
    background: radial-gradient(  rgba(203, 162, 95, 0.683) -60%,  rgba(0,0,0,0) 90% );
}
.main-block .main-block-item:nth-child(1){
    grid-area: 1/1/4/1;
}
.main-block .main-block-item:nth-child(2){
    grid-area: 1/2/3/3;
}
.main-block .main-block-item:nth-child(3){
    grid-area: 1/3/4/4;
}
.main-block .main-block-item:nth-child(4){
    grid-area: 4/1/5/1;
    width: 40px;
    margin: 0 auto;
    border-radius: 60px;
    height: 40px;
    padding: 4px;
}
.main-block .main-block-item:nth-child(5){
    grid-area: 3/2/4/3;
    width: 40px;
    margin: 0 auto;
    border-radius: 60px;
    height: 40px;
    padding: 4px;
}
.main-block .main-block-item:nth-child(6){
    grid-area: 4/3/5/4;
    width: 40px;
    margin: 0 auto;
    border-radius: 60px;
    height: 40px;
    padding: 4px;
}
.main-block .main-block-item:nth-child(7){
    grid-area: 5/1/7/1;
}
.main-block .main-block-item:nth-child(8){
    grid-area: 4/2/7/3;
}
.main-block .main-block-item:nth-child(9){
    grid-area: 5/3/7/4;
}

.main-block{
    position: relative;
    padding:    20px 10px 10px 20px;
    gap: 10px;
    grid-area: 1/1/7/4;
    display: grid;
    grid-template: repeat(6, 1fr) / repeat(3, 1fr);
    
    background-color: #211a14; 
    margin-right: 1px;
    /* border-radius:  0   0 10px 0; */
    border-radius:10px ;
}
.storage-wrap{
    background: radial-gradient(  rgba(203,162,95,1) 0%, rgba(203, 162, 95, 0.304) 40%, rgba(0,0,0,0) 70% );
    
    height: 100%;
    border: 2px solid #936f4b;
    border-radius: 6px;
    background-color: #211a14;
    position: relative;
    display: grid;
    grid-template: repeat(7, 1fr) / repeat(4, 1fr);
    /* overflow: hidden; */
}
.right-block{
   
    grid-area: 1/4/8/5;
    position: relative;
    padding:  10px 10px 20px 20px;
    gap: 10px;
    display: grid;
    grid-template: repeat(7, 1fr)/  1fr;
    background-color: #211a14; 
    border-radius:10px ;

    padding:    20px 20px 20px 10px;
}
.bottom-block{
    position: relative;
    padding:  10px 10px 20px 20px;
    gap: 10px;
    grid-area: 7/1/8/4;
    display: grid;
    grid-template: 1fr / repeat(6, 1fr);
    
    background-color: #211a14; 
    margin-top: 1px;
    margin-right: 1px;
    border-radius:10px ;
    /* border-radius:  0 10px  0  0; */
}
</style>