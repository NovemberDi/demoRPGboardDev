<template>
    <div class="stat-wrap">
        <div class="top">
            <div class="ower-top">
                <div class="activ">Персонаж</div>
                <div>Перки</div>
                <div>Эффекты</div>
            </div>
            <div class="name">
                Варя Оползень
            </div>
            <div class="user-info">
               <p>Уровень 14</p> 
               <p>Человек-Маг</p>
            </div>
            <div class="bars">
                <ProgressBar id="bar" :type="'HP'">HP 8/10</ProgressBar>
                <ProgressBar id="bar" :type="'EP'">HP 8/10</ProgressBar>
            </div>
            <div class="title-after">
                <p>Приключение: Золотая пещера</p>
                <p>Влделец: id235544343</p>
            </div>
        </div>
        <div class="bottom">
            <div class="bottom-top-wrap">
                    <div class="left">
                        <p>Характеристики</p>
                        <div class="characters">
                            <div>
                                <img src="./../assets/character/1.png" alt="">
                                <p>4</p>
                            </div>
                            <div>
                                <img src="./../assets/character/2.png" alt="">
                                <p>8</p>
                            </div>
                            <div>
                                <img src="./../assets/character/3.png" alt="">
                                <p>5</p>
                            </div>
                            <div>
                                <img src="./../assets/character/4.png" alt="">
                                <p>6</p>
                            </div>
                            <div>
                                <img src="./../assets/character/5.png" alt="">
                                <p>6</p>
                            </div>
                            <div>
                                <img src="./../assets/character/6.png" alt="">
                                <p>11</p>
                            </div>
                        </div>
                    </div>
                    <div class="right">
                        <p>Боевые навыки</p>
                        <div class="war-skils">
                            <div class="war-skils-item">
                                <div> <p>Атака</p> <p>7</p> </div>
                            </div>
                            <div class="war-skils-item">
                                <div> <p>Защита</p> <p>2</p> </div>
                            </div>
                            <div class="war-skils-item">
                                <div> <p>Сила заклинаний</p> <p>4</p> </div>
                            </div>
                            <div class="war-skils-item">
                                <div> <p>Сопротивляемость</p> <p>76</p> </div>
                            </div>
                            <div class="war-skils-item">
                                <div> <p>Скорость</p> <p>3</p> </div>
                            </div>
                        </div>
                    </div>
                
            </div>
            <div class="bottom-bottom-wrap">
                <p>Мирные навыки</p>
                <div class="peas-skils">
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/1.png" alt=""> 
                        <p>8</p> 
                    </div>
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/2.png" alt=""> 
                        <p>7</p> 
                    </div>
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/3.png" alt=""> 
                        <p>7</p> 
                    </div>
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/4.png" alt=""> 
                        <p>8</p> 
                    </div>
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/5.png" alt=""> 
                        <p>5</p> 
                    </div>
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/6.png" alt=""> 
                        <p>5</p> 
                    </div>
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/7.png" alt=""> 
                        <p>6</p> 
                    </div>
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/8.png" alt=""> 
                        <p>5</p> 
                    </div>
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/9.png" alt=""> 
                        <p>4</p> 
                    </div>
                    <div class="peas-skils-item">
                       <img src="./../assets/skils/10.png" alt=""> 
                        <p>2</p> 
                    </div>
     
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Stat'
    }
</script>

<style scoped>
.bottom-bottom-wrap{
    color:#978e7e;
}
.peas-skils-item {
    position: relative;
    color:#fff;
}
.peas-skils-item img{
    height: 30px;
    border: #978e7e 2px solid;
    border-radius: 4px;
}
.peas-skils-item p{
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translate(-50%, 25%);
    background-color: #211a14;
    height: 20px;
    width: 20px;
    border: #978e7e 2px solid;
    border-radius: 20px;
    font-size: 14px;
    font-weight: 500;
    line-height: 22px;
}
.peas-skils{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
    gap:10px;
    margin-top: 10px;
}
.war-skils-item div{
    display: flex;
    justify-content: space-between;
    align-items:flex-end;
    width: 100%;
    height: 14px;
    background-color: #211a14;
    position: absolute;
    top: 0;
    left: 0;
}
.war-skils-item{
    background: radial-gradient(at bottom,  rgba(203,162,95,1) 0%, rgba(203, 162, 95, 0.304) 40%, rgba(0,0,0,0) 70% );
    height: 15px;
    width: 100%;
    margin-top: 3px;
    margin-left: 20px;
    position: relative;
}
.war-skils .war-skils-item:last-child {
    background: none;
}
.war-skils{
    margin-top: 6px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 12px;

    
}
.characters{
display: grid;
grid-template-columns: 1fr 1fr;
gap:10px;
margin-top: 10px;
}
.characters div{
    display: flex;
    width: 40px;
    justify-content: space-between;
}
.characters img{
    height: 20px;
}
.bottom-top-wrap{
    height: 120px;
    width: 250px;
    margin: 20px auto 8px auto;
    display: flex;
    justify-content: space-between;
    font-size: 14px;
    color:#978e7e;
    background: radial-gradient(at bottom,  rgba(203,162,95,1) 0%, rgba(203, 162, 95, 0.304) 40%, rgba(0,0,0,0) 70% );
}
.left{
    background-color: #211a14;
    height: calc(100% - 1px);
    border-radius:  0 0 10px 0 ;
    width: 45%;

}
.right{
    background-color: #211a14;
    height: calc(100% - 1px);
    border-radius:  0  0  0 10px;
    width: calc(55% - 1px);
}
.bottom{
    margin-top: 6px;
    height: calc(100% - 136px);
    border: 2px solid #936f4b;
    border-radius: 6px;
    background-color: #211a14;

    position: relative;
}
.title-after{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 250px;
    font-size: 10px;
    color: #978e7e;
    margin-top: 6px;
    
}
.user-info{
    font-size: 12px;
    width: 250px;
    display: flex;
    justify-content: flex-start;
    align-items: center;    
    color: #a68245;
    margin-top: 6px;
}
.user-info p:last-child {
    color: #978e7e;
    margin-left: 6px;
}
.name{
    width: 250px;
    display: flex;
    font-size: 14px;
    margin-top: 6px;
}
.bars{
margin-top: 6px;
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
}
#bar{

}
.top{
    height: 126px;
    border: 2px solid #936f4b;
    border-radius: 6px;
    background-color: #211a14;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
}
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
}
.ower-top div{
    border: 2px solid #936f4b;
    border-radius: 10px;
    background-color: #211a14;
    height: 16px;
    font-size: 12px;
    letter-spacing: 1px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 10px;
    padding: 0 8px;
}
.activ{
    color: #ece8e1;
}
.stat-wrap{
    /* background-color: rgb(138, 127, 255); */
}
</style>