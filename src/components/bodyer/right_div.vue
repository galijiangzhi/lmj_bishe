<template>
    <div :style="bott_st" ref="bottSt">
        <div :style="[in_st, in_st_visible]" @click="triggerFileInput" @mouseenter="inin" @mouseleave="inout">
            <input ref="fileInput" type="file" @change="handleFileUpload" style="display: none;">
            <span>上传文件</span>
        </div>
        <div :style="[do_st, do_st_visible]" @mouseenter="doin" @mouseleave="doout" @click="saveImage">
            <span>保存文件</span>
        </div>
    </div>
</template>
<script>
export default{
    data(){
        return{
            bott_st:{
                position:"absolute",
                top:"700px",
                left:"1200px",
                fontSize:"40px",
            }
        }
    }
}
</script>
<style>

</style>