<template>
    <img class="logo" src="../../public/qhmulogo.png">
    <div class="div1">
        <span class="title">
            <Ttitle />
        </span>
    </div>
    <span class='test'>
        <h2 data-text="THE_APPLICATION_OF_LANGUAGE_MODELING_IN_TIBETAN_SCENE_OCR">THE_APPLICATION_OF_LANGUAGE_MODELING_IN_TIBETAN_SCENE_OCR</h2>
    </span>
</template>
<script>
    import Ttitle from "./header/title.vue"
        export default{
            components:{
                Ttitle,
            }
        }
</script>
<style scoped>
    .logo {
        height:80px;
        position:absolute;
        top:10px;
        left:20px;
        /* background: red; */
    }
    .div1{
        background:#111;
        width:calc(100vw - 700px);
        height:100px;
        position:absolute;
        left:700px;
    }
    .title {
        font-size: 50px;
        font-family: "微软雅黑", sans-serif;
        color:#000;
        font-weight: bold;
        position:absolute;
        top:15px;
        left:260px;
    }
    .test{
        position:absolute;
        font-size: 45px;
        background-color:#fff;
        width:100%;
        height:70px;
        top: 100px;
        text-align: center;
    }
    h2{
        position: relative;
        font-size: 40px;
        color:#999;
        background-color:#fff;
        -webkit-text-stroke:1px #382d52;
        text-transform: uppercase;
        position:absolute;
        z-index: 1;
        left:240px;
    }
    h2::before{
        /* 设置刷新之后的字体颜色 然后设置width 超出width的不显示 */
        content:attr(data-text);
        position: absolute;
        top: 0;
        left: 0;
        width: 0;
        height: 110%;
        color:#000;
        -webkit-text-stroke: 0vm #383d52;
        border-right: 2px solid #111;
        overflow:hidden;
        animation:animate 6s linear infinite;
        z-index: 2;
    }
    @keyframes animate{
        0%,10%,100%{
            width:0;
        }
        70%,90%{
            width:100%;
        }
    }
</style>