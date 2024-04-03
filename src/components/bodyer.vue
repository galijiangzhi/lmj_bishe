<template>
    <div class="left_div">
        <div :style="div1_st">
                <wind />
        </div>
    </div>
    <div class="right_div">
        <Right_div />
        <div :style="bott_st" ref="bottSt">
            <div :style="imgf">
                <img :style="imgdiv" v-if="imageUrl" :src="imageUrl"/>
            </div>
            <div :style="textdiv"></div>
            <div :style="in_st" @click="triggerFileInput" @mouseover="handleMouseE" @mouseout="handleMouseL">
                <input ref="fileInput" type="file" @change="handleFileUpload" style="display: none;">
                上传文件
            </div>
            <div :style="do_st" @mouseenter="doin" @mouseover="handleMouseE" @mouseout="handleMouseL">
                保存文件
            </div>
        </div>
    </div>
</template>
<script>
    import Right_div from "./bodyer/right_div.vue";
    import Wind from "./bodyer/wind.vue"
    import axios from 'axios'

    export default {
        data() {
            return {
                div1_st: {
                    pointerEvents:"none",
                    position:"relative",
                    top:"100px",
                    left:"30px",
                    height: "600px",
                    // backgroundColor: "lightblue",
                    display:"flex",
                    zIndex: "1",
                    // overflow: "hidden",
                },
                div2_st: {
                    flex: "1",
                    // backgroundColor: "lightgreen",
                    display: "flex",
                    flexDirection: "column",  // 将flex-direction设置为column
                    justifyContent: "flex-start",  // 垂直向上对齐
                    alignItems: "center",
                    overflow: 'auto' ,
                    background:"black",
                },
                in_st: {
                    position: "absolute",
                    top:"580px",
                    left:"200px",
                    width: "150px",
                    height: "50px",
                    backgroundColor: "rgba(20,20,20,0.7)",
                    display: "flex",
                    justifyContent: "center",
                    alignItems: "center",
                    cursor: "pointer",
                    boxShadowStyle:'none',
                    pointerEvents:"all",
                    color:"#fff",
                    boxShadow:"0 0 3px 1px rgba(255, 255, 255, 0.7)",
                    userSelect: "none"
                    // position: "absolute",
                },
                do_st: {
                    position: "absolute",
                    top:"580px",
                    left:"960px",
                    width: "150px",
                    height: "50px",
                    backgroundColor: "rgba(20,20,20,0.7)",
                    display: "flex",
                    justifyContent: "center",
                    alignItems: "center",
                    cursor: "pointer",
                    boxShadowStyle:'none',
                    pointerEvents:"all",
                    color:"#fff",
                    boxShadow:"0 0 3px 1px rgba(255, 255, 255, 0.7)",
                    userSelect: "none"
                    // position: "absolute",
                },
                imgf:{
                    position: "absolute",
                    left:"30px",
                    top:"30px",
                    width: "950px",
                    height: "510px",
                    display: "flex",
                    justifyContent: "center",
                    alignItems: "center",
                    // background:"red",
                    url:""
                },
                imgdiv:{
                    // width: "950px",
                    maxHeight:"100%",
                    maxWidth:"100%",
                    objectFit: "cover",
                    url:""
                },
                textdiv:{
                    position: "absolute",
                    left:"1010px",
                    top:"30px",
                    width: "310px",
                    height: "510px",
                    display: "flex",
                    justifyContent: "center",
                    alignItems: "center",
                    background:"red"
                },
                imageUrl: ''
            }
        },
        components:{
            Right_div,
            Wind,
        },
        methods:{
            handleMouseE(event){
                event.target.style.background = "rgba(150,150,150,0.5)";
                event.target.style.boxShadow = "0 0 10px 1px rgba(255, 255, 255, 0.7)";
            },
            handleMouseL(event){
                event.target.style.background = "rgba(20,20,20,0.7)";
                event.target.style.boxShadow = "0 0 3px 1px rgba(255, 255, 255, 0.7)";
            },
            triggerFileInput() {
                this.$refs.fileInput.click();
            },
            handleFileUpload(event) {
                const file = event.target.files[0];
                if (file) {
                    const reader = new FileReader();
                    reader.onload = (e) => {
                    this.imageUrl = e.target.result;
                    };
                    reader.readAsDataURL(file);
                }

                const formData = new FormData();
                this.imageUrl = null;
                formData.append('file', event.target.files[0]);

                axios.post('http://www.asuka.sanyueyu.top/lmj', formData, {
                headers: {
                    'Content-Type': 'multipart/form-data'
                },
                })
                .then(response => {
                // // 将后端返回的图片数据赋值给imageUrl
                console.log(response)
                // const blob = new Blob([response.data], { type: 'image/jpeg' }); // 创建Blob对象
                // this.imageBlob = blob; 
                // const imageUrl = URL.createObjectURL(blob); // 通过URL.createObjectURL将blob转换为URL
                // this.$data.showComponent=0,
                // this.imageUrl = imageUrl; // 将URL赋值给组件的imageUrl
                // })
                // .catch(error => {
                // // 处理错误
                // console.error('Error uploading file:', error);
                })
                .catch(error => {
                // 处理上传失败的逻辑
                console.log("shibai")
                });
            },

        }
    }
</script>
<style scoped>
    .left_div{
        height:100%;
        min-width:400px;
        background:black;
        display:flex;
        flex-direction:column
    }
    .right_div{
        position: absolute;
        left:500px;
        top:230px;
        height:640px;
        min-width:1350px;
        background:rgba(1,1,1,0.8);
        pointer-events:none;
        border-radius: 20px;
        z-index: 2;
        box-shadow: 0 0 10px #aaa,
                        0 0 20px #222,
                        0 0 40px #222,
                        0 0 50px #222;
        -webkit-box-reflect: below 5px linear-gradient(transparent,#555);
    }
</style>