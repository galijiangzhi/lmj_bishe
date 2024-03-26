<template>
    <div class="loader">
        <img src="../../../../public/头像.jpeg">
        <span class="img"></span>
        <span class="img"></span>
        <span class="img"></span>
    </div>
    <div class='text'>
        <div class="zdi">20计民班 拉马杰</div>
        <div class="zdi">指导教师：更太加</div>
        <div class="cj">主要荣誉：</div>
        <div class="jdi">2022 年获得第八届互联网＋校赛"金奖" </div>
        <div class="jdi">2021 年第十一届三创赛校赛“一等奖” </div>
        <div class="jdi">2021 计算机学院第十二届民族知识竞赛"二等奖" </div>
        <div class="jdi">2022 年获得第八届互联网＋高校主塞到省赛"银奖" </div>
        <div class="jdi">2022 年获得工业和信息化人才能力提升证书 </div>
        <div class="jdi">2022 年获得第十三届挑战杯国赛“铜奖”</div>
        <div class="jdi">2022 年获得筆八届互联网＋国赛“铜奖”</div>
        <div class="jdi">2022 年获得第十三届挑战杯省赛“三等奖” </div>
        <div class="jdi">2021 年第十—届三创赛校赛“最佳创意奖”</div>
        <div class="jdi">2023 年获得 2022~2023学年“优秀学生” </div>
        <div class="jdi">2021 年获得第十二届三创赛校赛"最佳创意奖" </div>
        <div class="jdi">2021 年获得计算机三级证书</div>
        <div class="jdi">2021 年荣获疫情防控优秀志愿者。</div>
    </div>
</template>
<script>
</script>
<style scoped>
    img{
        margin-top: 20px;
        height: 100px;
        width: 100px;
        border-radius: 50%;
        box-shadow:0 0 3px 1px rgba(255, 255, 255, 0.7);
    }
    .img{
        position:absolute;
        margin-top: 19px;
        left:149px;
        width:102px;
        height: 102px;
        border-radius:50%;
        background:linear-gradient(#111,#fff,#111,#fff);
        animation:animate 2s linear infinite;
        z-index: -1;
    }
    @keyframes animate{
        0%{
            transform: rotate(0deg);
        }
        100%{
            transform: rotate(360deg);
        }
    }
    .img:nth-child(1){
        filter:blur(1px);
        /* 模糊处理 */
    }
    .img:nth-child(2){
        filter:blur(3px);
    }
    .img:nth-child(3){
        filter:blur(5px);
    }
    .img:nth-child(4){
        filter:blur(7px);
    }
    .text{
        position:absolute;
        height:70%;
        width:100%;
        top:150px;
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
    .zdi:nth-child(2){
        margin-bottom: 30px;
    }
    .cj{
        font-size: 18px;
        margin-right: 210px;
        margin-bottom: 10px;
    }
    .jdi{
        display: flex;
        align-items: flex-start; /* 内部元素文本头部对齐 */
        width:100%;
        font-size: 14px;
        padding-left: 60px;
    }
</style>