<template>
    <div class="left_div">
        <div :style="div1_st">
            <button :style="but_st" @click="showComponent('Author')" class="button">作者信息</button>
            <button :style="but_st" @click="showComponent('Project')" class="button">项目介绍</button>
            <button :style="but_st" @click="showComponent('Technology')" class="button">主要技术</button>
            <button :style="but_st" @click="showComponent('Prospect')" class="button">未来展望</button>
            <button :style="but_st" @click="showComponent('xiangmutedian')" class="button">项目特点</button>
        </div>
        <div :style="div2_st">
        <component :is="selectedComponent" />
      </div>
    </div>
    <div class="right_div">
        <Right_div />
    </div>
</template>
<script>
    import Zuozhe from "./bodyer/zuozhe.vue";
    import Xiangmu from "./bodyer/xiangmu.vue";
    import Jishu from "./bodyer/jishu.vue";
    import Weilai from "./bodyer/weilai.vue";
    import xiangmu from "./bodyer/xiangmu.vue";
    import Right_div from "./bodyer/right_div.vue";

    export default {
        data() {
            return {
                div1_st: {
                    height: "60px",
                    // backgroundColor: "lightblue",
                    display:"flex",
                },
                but_st:{
                    flex:"1"
                },
                div2_st: {
                    flex: "1",
                    // backgroundColor: "lightgreen",
                    display: "flex",
                    flexDirection: "column",  // 将flex-direction设置为column
                    justifyContent: "flex-start",  // 垂直向上对齐
                    alignItems: "center",
                    overflow: 'auto' ,
                    background:"blue"
                },
            }
        },
        components:{
            Right_div,
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
        height:100%;
        flex:1;
        background:pink;
    }
</style>