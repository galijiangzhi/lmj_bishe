<template>
    <div class="div1" id="div1">
        <div class="div2" style="--i:1">
            <div class="div3">作者介绍</div>
        </div>
        <div class="div2" style="--i:2">
            <div class="div3">项目介绍</div>
        </div>
        <div class="div2" style="--i:3">
            <div class="div3">项目技术</div>
        </div>
        <div class="div2" style="--i:4">
            <div class="div3">项目特点</div>
        </div>
        <div class="div2" style="--i:5">
            <div class="div3">未来展望</div>
        </div>
    </div>
    <button :style="shunzhuan" @click="rotateDivshun">
        <svg :style="shun_svg" t="1711447908189" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="1596" ><path d="M238.208798 504.759085c114.078175 125.190257 330.334497 341.639984 441.040878 454.927143L785.790178 856.32207c-36.308951-36.902468-343.031681-348.783685-344.618828-358.506117 62.496379-64.083527 246.805082-251.967662 324.579423-339.65784l-95.228875-93.844342L238.208798 504.759085z" fill="#272636" p-id="1597"></path></svg>
    </button>
    <button :style="nizhuan" @click="rotateDivni">
        <svg :style="ni_svg" t="1711447908189" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="1596" ><path d="M238.208798 504.759085c114.078175 125.190257 330.334497 341.639984 441.040878 454.927143L785.790178 856.32207c-36.308951-36.902468-343.031681-348.783685-344.618828-358.506117 62.496379-64.083527 246.805082-251.967662 324.579423-339.65784l-95.228875-93.844342L238.208798 504.759085z" fill="#272636" p-id="1597"></path></svg></button>
</template>
<script>
export default {
    data(){
        return{
            shunzhuan:{
                height:"50px",
                width:"50px",
                // background:"red",
                borderRadius:"15px",
                zIndex:"10",
                border:"0",
                pointerEvents:"all",
                display:"flex",
                position: "absolute",
                top:"550px",
                left:"350px",
                justifyContent: "center", /* 水平居中 */
                alignItems: "center" /* 垂直居中 */
                
            },
            nizhuan:{
                height:"50px",
                border:"0",
                width:"50px",
                // background:"#555",
                borderRadius:"15px",
                position: "absolute",
                top:"550px",
                zIndex:"10",
                pointerEvents:"all",
                display:"flex",
                justifyContent: "center", /* 水平居中 */
                alignItems: "center" /* 垂直居中 */
            },
            shun_svg:{
                transform:"rotate(180deg)",
                height:"30px"
            },
            ni_svg:{
                height:"30px",
            }
        }
    },
    methods: {
        rotateDivshun() {
            let div1 = document.getElementById('div1');
            div1.style.transform += 'rotate(72deg)';
        },
        rotateDivni() {
            let div1 = document.getElementById('div1');
            div1.style.transform += 'rotate(-72deg)';
        }
    }
}
</script>
<style scoped>
        .div1{
            position: relative;
            top:700px;
            left:30;
            /* background: pink; */
            height: 300px;
            width: 300px;
            transition: transform 2s;
            /* animation: animateBg 10s linear infinite;
            animation-iteration-count: 1; */
        }
        /* @keyframes animateBg{
            0%{
                transform:rotate(0deg);
            }
            80%,100%{
                transform: rotate(360deg);
            }
        } */
        .div2{
            position: absolute;
            top:0;
            left:0;
            height: 100%;
            width: 100%;
            transform: rotate(calc(72deg * var(--i)));
        }
        .div3{
            position:absolute;
            height: 600px;
            border-radius: 20px;
            width:400px;
            background: rgba(51,51,51,0.5);
            top:-700px;
            pointer-events: none;
            box-shadow: 0 0 10px #aaa,
                        0 0 20px #aaa,
                        0 0 30px #aaa,
                        0 0 40px #aaa,
                        0 0 50px #aaa,
                        0 0 60px #aaa,
                        0 0 170px #aaa;
        }
</style>