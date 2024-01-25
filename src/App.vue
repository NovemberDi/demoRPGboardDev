<template>
  <Header id="header"></Header>
  <img id="back" src="https://habrastorage.org/getpro/freelansim/allfiles/18/180/180655/playerscreen.jpeg" alt="">
  <MyBoard></MyBoard>

</template>

<script>


export default {
  name: 'App',

}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Jost:wght@100;300;600&display=swap');

* {
margin: 0;
padding: 0;
font-family: 'Jost', sans-serif;
}
#header{
  position: absolute;
  top: 0;
  left: 0;
}
#back{
  position: absolute;
  top: 0;
  left: 50%;
  transform: translate(-50%, 0);

  height: 100%;
 
  opacity: 0.3;
  z-index: 500;
  display: none;
}
#app {
background-image: url('./assets/back.png');
background-repeat: no-repeat;
background-size:cover;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #313338;

  height: 770px;
  width: 1600px;
  min-height: 100vh;
  min-width: 100vw;
  color: #ffffff ;
}
</style>
