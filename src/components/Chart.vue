<template>
    <div class="chart-wrap">
        <p class="chart-title">Харизма</p>
        <canvas id="chart-canvas" width="320" height="210" ref="canvas"></canvas>
        <div class="img-box girl">
            <img src="./../assets/girl.png" alt="">
        </div>
        <div class="img-box orck">
            <img src="./../assets/orck.png" alt="">
        </div>
        <div class="img-box elf">
            <img src="./../assets/elf.png" alt="">
        </div>
        
    </div>
</template>

<script>
    export default {
        name: 'Chart',
        methods:{
            drowChart(){
                let ctx = this.$refs.canvas.getContext('2d');
                let canvasWidth = this.$refs.canvas.clientWidth;
                let canvasHeight = this.$refs.canvas.clientHeight;
                let startPoint = {
                    x: Math.round(canvasWidth/2),
                    y: Math.round(canvasHeight/2+6),
                };

                function calculatePoints(dia){
                    let shift = Math.tan((Math.PI*30)/180) * dia;
                    let arr =[
                    {x:startPoint.x - shift, y:(startPoint.y - dia)},
                    {x:startPoint.x + shift, y:(startPoint.y - dia)},
                    {x:startPoint.x + shift*2, y:(startPoint.y)},
                    {x:startPoint.x + shift, y:(startPoint.y + dia)},
                    {x:startPoint.x - shift, y:(startPoint.y + dia)},
                    {x:startPoint.x - shift*2, y:(startPoint.y)},   
                ]
                    return arr
                };

                let outerPoint = calculatePoints(85)

                ctx.strokeStyle = '#936f4b';
                ctx.lineWidth =  1;
                //контур
                ctx.lineWidth = 2;
                ctx.beginPath();                
                ctx.moveTo(outerPoint[0].x, outerPoint[0].y);
                ctx.lineTo(outerPoint[1].x, outerPoint[1].y);
                ctx.lineTo(outerPoint[2].x, outerPoint[2].y);
                ctx.lineTo(outerPoint[3].x, outerPoint[3].y);
                ctx.lineTo(outerPoint[4].x, outerPoint[4].y);
                ctx.lineTo(outerPoint[5].x, outerPoint[5].y);
                ctx.lineTo(outerPoint[0].x, outerPoint[0].y);  
                ctx.stroke();
                ctx.closePath();

                ctx.fillStyle = '#c39f7b';
                ctx.fillText('ТСЛ', outerPoint[0].x - 35, outerPoint[0].y);
                ctx.fillText('ЭНР', outerPoint[1].x + 14, outerPoint[1].y);
                ctx.fillText('ПСИ', outerPoint[2].x + 14, outerPoint[2].y + 3);
                ctx.fillText('ИНТ', outerPoint[3].x + 14, outerPoint[3].y + 6);
                ctx.fillText('ДУХ', outerPoint[4].x - 35, outerPoint[4].y + 6);
                ctx.fillText('КРД', outerPoint[5].x - 35, outerPoint[5].y + 3);
                

                //лучи
                ctx.lineWidth = 1;
                ctx.setLineDash([3, 4]);
                ctx.beginPath(); 
                    ctx.strokeStyle = '#ff6f4b';               
                    ctx.moveTo(startPoint.x, startPoint.y); ctx.lineTo(outerPoint[0].x, outerPoint[0].y);
                    ctx.stroke();
                ctx.closePath();
                ctx.beginPath();
                    ctx.strokeStyle = '#33ff4b';  
                    ctx.moveTo(startPoint.x, startPoint.y); ctx.lineTo(outerPoint[1].x, outerPoint[1].y);
                    ctx.stroke();
                ctx.closePath();
                ctx.beginPath(); 
                    ctx.strokeStyle = '#a826d3';               
                    ctx.moveTo(startPoint.x, startPoint.y); ctx.lineTo(outerPoint[2].x, outerPoint[2].y);
                    ctx.stroke();
                ctx.closePath();
                ctx.beginPath();
                    ctx.strokeStyle = '#2662d3';  
                    ctx.moveTo(startPoint.x, startPoint.y); ctx.lineTo(outerPoint[3].x, outerPoint[3].y);
                    ctx.stroke();
                ctx.closePath();
                ctx.beginPath(); 
                    ctx.strokeStyle = '#d3cd26';               
                    ctx.moveTo(startPoint.x, startPoint.y); ctx.lineTo(outerPoint[4].x, outerPoint[4].y);
                    ctx.stroke();
                ctx.closePath();
                ctx.beginPath();
                    ctx.strokeStyle = '#ef7b28';  
                    ctx.moveTo(startPoint.x, startPoint.y); ctx.lineTo(outerPoint[5].x, outerPoint[5].y);
                    ctx.stroke();
                ctx.closePath();
                
                //контур 2
                ctx.setLineDash([]);
                ctx.strokeStyle = 'rgba(80,80,80,0.3)';
                ctx.lineWidth = -2;
                outerPoint = calculatePoints(55);
                ctx.beginPath();                
                ctx.moveTo(outerPoint[0].x, outerPoint[0].y);
                ctx.lineTo(outerPoint[1].x, outerPoint[1].y);
                ctx.lineTo(outerPoint[2].x, outerPoint[2].y);
                ctx.lineTo(outerPoint[3].x, outerPoint[3].y);
                ctx.lineTo(outerPoint[4].x, outerPoint[4].y);
                ctx.lineTo(outerPoint[5].x, outerPoint[5].y);
                ctx.lineTo(outerPoint[0].x, outerPoint[0].y);  
                ctx.stroke();
                ctx.closePath();

                //область
                ctx.strokeStyle = '#936f4b';
                let areaPoints = [
                    {x: startPoint.x - 65, y: startPoint.y - 10},
                    {x: startPoint.x - 40, y: startPoint.y - 40},
                    {x: startPoint.x - 0, y: startPoint.y - 40},
                    {x: startPoint.x + 20, y: startPoint.y - 10},
                    {x: startPoint.x - 3, y: startPoint.y + 14},
                    {x: startPoint.x - 33, y: startPoint.y + 20},
                    {x: startPoint.x - 65, y: startPoint.y - 10},
                ]
                
                ctx.beginPath();                
                ctx.moveTo(areaPoints[0].x, areaPoints[0].y);
                for(let i = 1; i < areaPoints.length; i++){
                ctx.lineTo(areaPoints[i].x, areaPoints[i].y);
                }
                ctx.fillStyle = '#454545';
                ctx.fill();
                ctx.stroke();
                ctx.closePath();

                let titleArr = [5,5,5,5,5,7]
                    ctx.font = '8pt Arial';
                    ctx.textAlign = 'center';

                for(let i = 1; i < areaPoints.length; i++){
                    ctx.beginPath(); 
                    ctx.arc(areaPoints[i].x, areaPoints[i].y, 3, 0, Math.PI * 2);
                    // ctx.stroke();
                    ctx.fillStyle = '#936f4b';
                    ctx.fill();
                    ctx.closePath();
                }
                for(let i = 1; i < areaPoints.length; i++){
                    ctx.fillText(titleArr[i-1], areaPoints[i].x, areaPoints[i].y-7);
                }

            },
 
        },
        mounted(){
            this.drowChart();
        }
    }
    
</script>

<style scoped>
.img-box{
    position: absolute;
    overflow: hidden;
    height: 30px;
    width: 30px;
    border-radius: 25px;
    border: #936f4b 1px solid;
}
.img-box img{
height: 100%;
}
.girl{
    top: calc(50% - 10px);
    left: calc(50% - 17px);
}
.orck{
    top: 14px;
    left: 98px;
}
.elf{
    top: calc(50% - 10px);;
    left: 52px;
}
.chart-title{
    position: absolute;
    top: 0;
    left: 50%;
    transform: translate(-50%, 0);
    font-size: 14px;
    color:#978e7e;

}
#chart-canvas{
margin: auto;
}
.chart-wrap{
    /* border: 3px solid #605440; */
    height: 100%;
    border: 2px solid #936f4b;
    border-radius: 6px;
    background-color: #211a14;
    position: relative;
    display: grid;
    grid-template: repeat(4, 1fr) / repeat(15, 1fr);
    overflow: hidden;
}
</style>