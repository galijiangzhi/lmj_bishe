<template>
    <div class='text'>
        <div class="zdi">研究展望</div>
        <div class="jdi">
            近年来，随着技术的不断发展和应用场景的扩大，藏文场景OCR技术取得了显著的进展和应用。在研究过程中，也发现了一些存在的问题和挑战。
        </div>
        <div class="jdi">
            在语言建模方法方面，当前主要使用的是基于统计的方法，如n-gram模型。虽然这种方法在一定程度上能够适应藏文语言的特点，但仍然存在一些不足之处，
            于是未来的研究可以探索更加先进的语言建模方法，如神经网络模型，来提升藏文OCR的准确性和鲁棒性。
        </div>
        <div class="jdi">
            在数据集构建方面，目前可用的藏文语料库相对有限，并且存在语料质量不高的问题。进一步研究应该加强对藏文语料库的整理和标注工作，
            以提高数据集的质量和规模，从而为语言建模提供更强大的支持。
        </div>
        <div class="jdi">
            在模型训练与优化方面，目前主要是使用传统的机器学习算法进行训练和优化。但是这种方法受限于特征提取方法的局限性，导致模型性能的提升空间有限。
            因此，未来的研究可以尝试引入深度学习方法，结合更多的特征信息来进行模型训练与优化，以进一步提升藏文OCR的性能。
        </div>
        <div class="jdi">
            总之，藏文场景OCR中的语言建模应用是一个富有挑战性和潜力的研究方向。通过进一步研究，有望进一步提升藏文OCR的准确性和鲁棒性，
            拓展其在不同领域的应用，为藏文信息处理和传播做出更大的贡献。</div>
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
    }，
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
        font-size: 13px;
        padding-left: 30px;
        padding-right: 30px;
    }
</style>