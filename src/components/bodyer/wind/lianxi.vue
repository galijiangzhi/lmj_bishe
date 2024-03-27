<template>
    <div class='text'>
        <div class="zdi">联系我们</div>
        <div class="cj">
            <div class="te">您可以用过以下方式联系我们，我们诚切期待与您的沟通交流！！！</div>
            <div class="jdi">
                <img src="../../../../public/电话.png" >
                <div class="numb">187 9724 2833</div>
            </div>
            <div class="jdi">
                <img src="../../../../public/邮箱.png" >
                <div class="numb">2574894405@qq.com</div>
            </div>
            <div class="jdi">
                <img src="../../../../public/微信.png" >
                <div class="numb">Balmaskaybs</div>
            </div>
            <div class="jdi">
                <img src="../../../../public/球球.png" >
                <div class="numb">2574894405</div>
            </div>
            <div class="jdi">
                <img src="../../../../public/邮筒.png" >
                <div class="numb">810007</div>
            </div>
        </div>

    </div>
</template>
<script>
</script>
<style scoped>
    .text{
        position:absolute;
        height:70%;
        width:100%;
        top:40px;
        display: flex;
        flex-direction: column; /* 内部元素从上到下排列 */
        align-items: center; /* 水平居中对齐 */
        justify-content: flex-start; /* 垂直向上对齐 */
        color:white;
        
        /* background: pink; */
    }
    .zdi{
        font-size: 20px;
    }
    .zdi:nth-child(1){
        margin-bottom: 50px;
    }
    .cj{
        position: relative;
        height: 100px;
        width:100%;
        /* background: pink; */
    }
    .te{
        font-size: 15px;
        padding-left: 60px;
        padding-right: 60px;
        text-indent:30px;
        margin-bottom: 20px;
    }
    .jdi{
        height:70px;
        /* background-color: aqua; */
        text-indent:30px;
        display: flex;
        width:100%;
        font-size: 15px;
        padding-left: 60px;
        padding-right: 60px;
        align-items: center; /* 垂直居中对齐 */
        justify-content: space-between; /* 水平头对齐 */
    }
    img{
        height: 40px;
    }
    .numb{
        width:325px;
        /* background-color: blue; */
        font-size: 26px;
    }
</style>