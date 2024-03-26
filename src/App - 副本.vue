<script>
import Header from "./components/header.vue"
import Bodyer from "./components/bodyer.vue"
import Footer from "./components/footer.vue"
import Tees from "./components/test.vue"
export default{
  data(){
    return{
      root_css:{
        height:"100vh",
        width:"100vw",
        // background:"black",
        display:"flex",
        flexDirection:"column",
        overflow: "hidden",

      },
      head_css:{
        height:"170px",
        // background:"pink",,
        width:"100%"
      },
      body_css:{
        minHeight:"400px",
        width:"100%",
        // background:"green",
        flex:"1",
        display:"flex"
      },
      foot_css:{
        height:"70px",
        width:"100%",
        background:"yellow"
      }
    }
  },
  components:{
    Header,
    Bodyer,
    Footer,
    Tees,
  }
}
</script>
<template>
  <div :style="root_css">
    <div :style="head_css">
      <Header />
    </div>
    <div :style="body_css">
      <!-- <Bodyer /> -->
      <Tees />
    </div>
    <div :style="foot_css">
      <Footer />
    </div>
  </div>
</template>
<style scoped>
*{
  border:0;
  
}
</style>
