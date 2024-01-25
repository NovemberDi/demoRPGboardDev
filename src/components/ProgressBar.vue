<template>
    <div class="progress-wrap">
        <div class="bar" 
        :class="{
            'red-bar': type == 'HP',
            'yellow-bar': type == 'EP'
            }">
            <div class="loader"
            :class="{
            'red-loader': type == 'HP',
            'yellow-loader': type == 'EP'
            }"
            ></div>
            <div class="title"> 
                <slot></slot>
            </div>
           
        </div>
    </div>
</template>

<script>
    export default {
        name: "ProgressBar",
        props:{
            type:{Type: String}
        }

    }
</script>

<style scoped>
.title{
    position: absolute;
    font-size: 12px;
    top:50%;
    left:50%;
    transform: translate(-50%, -50%);
}
.bar{
    height: 10px;
    width: 250px;
    margin: 4px 0;
    border-radius: 12px;
    position: relative;
    overflow: hidden;
}
.loader{
    position: absolute;
    height: 12px;
    width: 100%;
    
    border-radius: 12px;
    position: relative;
    top: 0;
    left: -20%;
}
.red-bar{
    background-color: rgb(87, 20, 20);
    border: 1px solid rgb(140, 46, 46);
}
.red-loader{
    background: linear-gradient(90deg, rgba(87, 32, 32, 0) 0%, rgb(199, 17, 17) 100%);
}
.yellow-bar{
    background-color: rgb(109, 97, 84);
    border: 1px solid rgb(163, 130, 95);
}
.yellow-loader{
    background: linear-gradient(90deg, rgba(87, 32, 32, 0) 0%, rgb(247, 167, 38) 100%);
}
</style>