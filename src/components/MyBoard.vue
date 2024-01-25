<template>
    <div class="board-wrap">
        <div class="board">
            <Ava id="ava"></Ava>
            <Stat id="stat"></Stat>
            <Storage id="storage"></Storage>
            <Chat id="chat"></Chat>
            <Chart id="chart"></Chart>
            <Lotes id="lotes"></Lotes>

            
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MyBoard'
    }
</script>

<style scoped>
#ava{
    grid-area: 1 / 1 / 1 / 1;
}
#stat{
    grid-area: 1 / 2 / 1 / 2;
}
#storage{
    grid-area: 1 / 3 / 3 / 4;
}
#chat{
    grid-area: 1 / 4 / 4 / 5;
}
#chart{
    grid-area: 2 / 2 / 4 / 2;
}
#lotes{
    grid-area: 3 / 3 / 3 / 4;
}
.board-wrap{
    position: absolute;
  top: 0;
  left: 50%;
  transform: translate(-50%, 0);

  height: 100%;
    
}
.board{
    /* background-color: azure; */
    /* opacity: 0.4; */
    display: grid;
    grid-template: 430px 42px 150px / 150px 324px 674px 324px ;
    gap: 17px;
    height: calc(100vh - 100px);
    width: calc(100vw - 70px);
    margin: 60px auto 60px auto;
}
</style>