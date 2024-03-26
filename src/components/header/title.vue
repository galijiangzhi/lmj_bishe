<template>
    <div class="loader">
        <div class="ti"></div>
    </div>
</template>
<script></script>
<style scoped>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    .ti{
        height: 80px;
        width:760px;
        /* background: white; */
        position:relative;
        /* background:pink; */
        overflow: hidden;
        border-radius: 20px;
    }
    .ti:after{
        content: "";
        position: absolute;
        left:-100px;
        top:-550px;
        border-radius: 50%;
        height:1000px;
        width:1000px;
        background-color:pink;
        z-index: 1;
        filter:blur(20px);
        animation:animate 7s linear infinite;
        background:linear-gradient(#111,#fff,#fff,#111,#fff,#111,#fff,#fff);
    }
    .ti:before{
        content: "藏文场景OCR中的语言建模应用";
        color: white;
        font-size: 50px;
        position: absolute;
        left:2px;
        top:2px;
        height:76px;
        width:756px;
        background-color:black;
        z-index: 2;
        border-radius: 20px;
        display: flex;
        justify-content: center; /* 水平居中 */
        align-items: center; /* 垂直居中 */
    }
    @keyframes animate{
        0%{
            transform: rotate(0deg);
        }
        100%{
            transform: rotate(360deg);
        }
    }
</style>