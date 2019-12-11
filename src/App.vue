<template>
  <div id="app">
    <header>
      <img src="./assets/cross.svg"/>
      <h1>TH 151 Finals</h1>
      <h1>Cobbie's Catholic Creed</h1>
    </header>
    <!-- <div id="cross-container"></div> -->

  <div id="content-container">
    <p v-on="{mouseover: showExp, mouseleave: showExp}" class="content">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
    <p v-if="visible===true" class="explanation">Nam gravida eu mi sit amet viverra. Nam ut libero quis ligula eleifend egestas. In posuere, massa at cursus blandit, libero quam lobortis lorem, a egestas arcu ex vitae ipsum. Vestibulum auctor placerat lorem et scelerisque. Praesent non tincidunt sem.</p>
    <p class="content">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
    <p class="content">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
    <p class="content">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
    <p class="content">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
  </div>
  </div>
  
    
</template>

<script>
export default {
  name: 'app',
  methods: {
    showExp: function(){
      this.visible = !this.visible
    }
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      visible: false
    }
  }
}
</script>

<style> 
body{
  background-color:#1c253c;
}

#app{
  width: 100%;
}
#cross-container{
  display: flex;
  justify-content: center
}


header{
  color: white;
  font-family: Merriweather;
  text-align: center;
  width: 100%;
  margin: 0 auto
}
img{
  height: 50px;
  margin: 0 auto;
  margin-top: 20px;
}
h1{
  /* margin-top: -1px; */
}

#content-container{
  padding-top: 20px;
  color: white;
  height: 500px;
  font-family: 'Open Sans';
  width: 760px;
  margin: 0 auto;

}
p{
  padding-top: 9px;
  cursor: pointer;
}
p:hover{
  background-color:	#3c1c31;
}

</style>
