<template>
    <div class='text'>
        <div class="zdi">技术介绍</div>
        <div class="jdi">为了能够更好的识别场景藏文字，本项目基于英文的预训练模型ABInet进行场景文字的识别。
            首先，是自主阻止梯度在视觉和语言模型之间流动，以确保语言建模的准确执行。其次，提出了一种新型双向完形填空网络（BCN），
            其基于双向特征表示，作为语言模型的一部分。第三，提出了一种语言模型迭代校正的策略，旨在有效减轻来自噪声输入的影响。此外，
            通过迭代预测的集成，提出了一种自我训练方法，能够有效地从未标记的图像中学习。通过收集各种场景中的藏文图像，并进行标记，包括室内、
            室外、不同光照条件下的照片，以及不同角度和距离下的图像。收集大量的语料库作为实验的支撑。实验结果表明，ABINet 在低质量图像上具有优势，
            并在几个主流基准上取得了最先进的结果。
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
        margin-bottom: 30px;
    }
    .cj{
        font-size: 18px;
        margin-right: 210px;
        margin-bottom: 10px;
    }
    .jdi{
        text-indent:30px;
        display: flex;
        align-items: flex-start; /* 内部元素文本头部对齐 */
        width:100%;
        font-size: 15px;
        padding-left: 60px;
        padding-right: 60px;
    }
</style>