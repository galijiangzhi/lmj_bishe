<template>
    <div class='text'>
        <div class="zdi">项目介绍</div>
        <div class="jdi">本项目主要研究了在藏文场景光学字符识别（Optical Character Recogn ition OCR）中应用语言建模的方法和技术。
            由于藏文信息处理技术的不断进步，对于藏文的识别已经取得了显著的进展。藏文场景文字识别是一项更广泛的任务，
            它涵盖了在各种场景中拍摄的藏文文本的检测和识别。这可能涉及到不同字体、不同大小、不同光照条件下的文字。目前的藏文识别还停留在视觉层面的识别，
            没有涉及到语言知识对场景文本识别的帮助。通过本项目的研究，可以提高藏文场景OCR的准确率和稳定性，为藏文的数字化处理提供更好的支持，并具有广泛的应用前景。
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
        margin-bottom: 35px;
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
        font-size: 16px;
        padding-left: 60px;
        padding-right: 60px;
        overflow-wrap: break-word;
    }
</style>