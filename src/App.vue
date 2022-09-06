<template>
 
 <div >
  <div class="wrapper" 
@mousemove="changeBackground" 
:style="{transform: `translate(-${backgroundMoveX}%)`}">
</div>

  <div class="container"
  @mousemove="changeBackground">
    <headerApp></headerApp>
    <contentApp></contentApp>
  </div>
 </div>



</template>


<script>


import headerApp from '@/components/headerApp.vue'
import contentApp from '@/components/contentApp.vue'

export default {
  name: 'App',
  data(){
  return{
    backgroundMoveX: 0,
     


  }
},
methods:{
  changeBackground(e) {
    const winWidth = window.innerWidth
    this.backgroundMoveX = e.pageX / (winWidth / 5)
    
  }


},
  components: {
    headerApp,
    contentApp
    
}
  
}

</script>

<style lang="scss">
ul,li{
  list-style-type: none;
  margin: 0;
  padding: 0;
}
a{
  text-decoration: none;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.container{
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px 0 15px;
}
.wrapper{
    top:0;
    left: 0;
    padding-right: 100px;
    position:absolute;
    width: 105%;
    min-height: 120vh;
    background: url(./img/image\ 3.png) no-repeat;
    background-position:center;
    background-size:cover;
    transition: all 300ms ease;
}


</style>
