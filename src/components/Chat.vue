<template>
    <div class="chat-wrap">
        <div class="ower-top">
                <div>Лобби</div>
                <div class="activ">Чат</div>
                <div>Журнал событий</div>
        </div>
        <div class="chat-head">
            <p>Лобби</p>
            <p>Присоединиться к лобби</p>
            <p>Чат</p>
        </div>
        <div class="income">
            <div class="msg">
                <img class="resend" resend src="./../assets/resend.svg" alt="">
                <p class="author green">Knikgt_Kott</p>
                <p class="msg-content">
                Я подхожу к загадочному колодцу и заглядываю внутрь. Я пытаюсь вглядеться в глубину колодца и понять, есть ли там что-то опасное...    
                </p>
            </div>
            <div class="back"></div> 
            <!-- <div class="outline"></div> -->
            <div class="msg-time">12:01</div>
        </div>

        <div class="income">
            <div class="msg">
                <!-- <p class="author green">Knikgt_Kott</p> -->
                <p class="msg-content">
                    Если всё хорошо, то пытаюсь <br>спуститься внутрь...
                </p>
            </div>
            <div class="back"></div> 
            <!-- <div class="outline"></div> -->
            <div class="msg-time">12:01</div>
        </div>

        <div class="outgoing">
            <div class="msg">
                <p class="msg-content w-240">
                    Не влезай, оно тебя сожрёт!!😓😓😓
                </p>
            </div>
            <div class="reverse-back"></div> 
            <!-- <div class="outline"></div> -->
            <div class="msg-time">12:01</div>
        </div>
        <div class="income">
            <div class="msg">
                <img class="resend" resend src="./../assets/resend.svg" alt="">
                <p class="author white">Tveyn <span>Мастер игры</span></p>
                <p class="msg-content">
                    Колодец безопасен. Бросай кубик на гимнастику, чтобы проверить успешность приземления.
                </p>
            </div>
            <div class="master-back"></div> 
            <div class="outline"></div>
            <div class="msg-time">12:01</div>
        </div>
        <div class="income">
            <div class="msg">
                <img class="resend" resend src="./../assets/resend.svg" alt="">
                <p class="author pink">Trixxterr_kitty</p>
                <div class="resended">
                    <Span>В ответ Knikgt_Kott</Span> <br>
                    Я подхожу к загадочному колодцу ...
                </div>
                <p class="msg-content">
                    Да ладно, лезь, что может случиться? В крайнем случае доставим твой труп и заберем твои вещи.😂😂😂
                </p>
            </div>
            <div class="back"></div> 
            <div class="msg-time">12:01</div>
        </div>
        <div class="sendler">
            <div class="input">Да он сейчас умрет просто|</div>
            <div class="button">Отправить</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Chat'
    }
</script>

<style scoped>
.sendler{
width: 94%;
height: fit-content;
position: absolute;
bottom: 16px;
left: 0;
display: flex;
justify-content: space-between;
margin: 0 10px;
}
.input{
    width: 70%;
    height: 30px;
    background-color: #2e241b;
    border-radius: 6px;
    border: 3px solid #605440;
    box-sizing: border-box;
    display: flex;
    justify-content: center;
    align-items: center;
}
.button{
    width: 30%;
    height: 30px;
    background-color: #605440;
    border-radius: 6px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 4px;
}
.resended span{
    color:#fff;
}
.resended{
    background-color: #2e241b;
    border-radius: 10px;
    width: 100%;
    height: 30px;
    font-size: 10px;
    padding: 5px;
}
.pink{
    color:#be6de9
}
.author{
    font-weight: 600;
}
.white{
    color: #fff;
}
.white span{
    color: #aa8057;
}
.master-back{
height: calc(100% - 2px);
width: calc(100% - 2px);
background-color: #2e241b;
border-radius: 10px;
position: absolute;
left: 50%;
top:50%;
transform: translate(-50%,-50%);
z-index: 5;
}
.master-back{
height: calc(100% - 2px);
width: calc(100% - 2px);
background-color: #2e241b;
border-radius: 10px;
position: absolute;
left: 50%;
top:50%;
transform: translate(-50%,-50%);
z-index: 5;
}
.master-back::after{
    content: '';
    position: absolute;
    left: -10px;
    /* right: -10px; */
    bottom: 0;
	width: 0;
	height: 0;
	border-left: 20px solid transparent;
	border-right: 20px solid transparent;
	border-bottom: 20px solid #2e241b;
}
.resend{
position: absolute;
top:-10px;
right: -10px;
height: 25px;
}
.w-240{
width: 240px;
}

.green{
    color: #44ff00;
}
.msg-time{
    position: absolute;
    right: 15px;
    bottom: 4px;
    z-index: 15;
}
.msg-content{

}
.msg{
display: flex;
flex-direction: column;
text-align: left;
position: relative;
z-index: 15;
width: 90%;
margin: 0 auto;
color: #c6bfb4;
}
.outgoing{
    position: relative;
    height: fit-content;
    min-height: 30px;
    width: fit-content;
    min-width: 210px;
    max-width: 268px;
    padding:  10px 0;
    margin-bottom: 8px;
    align-self: flex-end;
}
.income{
    position: relative;
    height: fit-content;
    min-height: 30px;
    width: fit-content;
    min-width: 210px;
    max-width: 268px;
    padding:  10px 0;
    margin-bottom: 8px;

}
.outline{
height: 100%;
width: 100%;
background-color: #936f4b;
border-radius: 10px;
position: absolute;
left: 50%;
top:50%;
transform: translate(-50%,-50%);
z-index: 0;


}
.outline::after{
    z-index: 0;
    content: '';
    position: absolute;
    left: -12px;
    bottom: 0;
	width: 0;
	height: 0;
	border-left: 20px solid transparent;
	border-right: 20px solid transparent;
	border-bottom: 20px solid #936f4b;
 
}
.back{
height: calc(100% - 2px);
width: calc(100% - 2px);
background-color: #4e3e31;
border-radius: 10px;
position: absolute;
left: 50%;
top:50%;
transform: translate(-50%,-50%);
z-index: 5;
}
.reverse-back{
height: calc(100% - 2px);
width: calc(100% - 2px);
background-color: #422d1c;
border-radius: 10px;
position: absolute;
left: 50%;
top:50%;
transform: translate(-50%,-50%);
z-index: 5;
}
.reverse-back::after{
    content: '';
    position: absolute;
    right: -10px;
    bottom: 0;
	width: 0;
	height: 0;
	border-left: 20px solid transparent;
	border-right: 20px solid transparent;
	border-bottom: 20px solid #422d1c;
}
.back::after{
    content: '';
    position: absolute;
    left: -10px;
    /* right: -10px; */
    bottom: 0;
	width: 0;
	height: 0;
	border-left: 20px solid transparent;
	border-right: 20px solid transparent;
	border-bottom: 20px solid #4e3e31;
}
.chat-head{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    margin-top: 12px;
    background-color: #211a14;
    box-shadow: 0px 5px 15px 5px #211a14 ;
    position: relative;
    z-index: 20;
}
.chat-head  p{
width: 100%;
height: 24px;
margin: 4px 0;
display: flex;
justify-content: center;
align-items: center;
}
.chat-head  p:nth-child(2){
    border: 3px solid #605440;
    border-radius: 6px;
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
.chat-wrap{
    /* border: 3px solid #605440; */
    height: 100%;
    border: 2px solid #936f4b;
    border-radius: 6px;
    background-color: #211a14;
    position: relative;
    padding: 0 20px;
    font-size: 12px;
    letter-spacing: 1px;

    display: flex;
    flex-direction: column;
}
</style>