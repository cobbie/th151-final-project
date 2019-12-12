<template>
  <div id="app">
    <header>
      <img class="animated fadeInUp delay-1s" src="./assets/cross.svg"/>
      <h1 class="animated fadeInUp delay-2s">TH 151 Finals</h1>
      <h1 class="animated fadeInUp delay-2s">Cobbie's Catholic Creed</h1>
      <button @click="showExp" class="animated flipInX delay-3s">Show explanations</button>
      <p class="animated flipInX delay-3s" id="note">You can also hover over each line in the creed to toggle the explanations.</p>
    </header>
    <!-- <div id="cross-container"></div> -->

  <div id="content-container">
    <p class="content animated fadeInLeftBig delay-4s" v-on="{mouseover: showExp, mouseleave: showExp}" >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
    <p v-if="visible===true" class="explanation animated zoomIn">Nam gravida eu mi sit amet viverra. Nam ut libero quis ligula eleifend egestas. In posuere, massa at cursus blandit, libero quam lobortis lorem, a egestas arcu ex vitae ipsum. Vestibulum auctor placerat lorem et scelerisque. Praesent non tincidunt sem.</p>
    <p class="content animated fadeInRightBig delay-2nd">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
    <p class="content animated fadeInLeftBig delay-3rd">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
    <p class="content animated fadeInRightBig delay-4th">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
    <p class="content animated fadeInLeftBig delay-5th">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent felis diam, facilisis tincidunt finibus quis, interdum et ex. Cras pulvinar tellus ac nulla convallis, at lacinia tellus tempus.</p>
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
  /* background-color:#1c253c; */
  background-color:black;
}

#app{
  width: 100%;
}
#cross-container{
  display: flex;
  justify-content: center
}
#note{
  font-family: Open Sans;
font-style: italic;
font-size: 13px;
line-height: 15px;
color: #ffffff

}

.explanation{
  /* width: 807px; */
height: 80px;
padding-left:20px;
background: rgba(31, 62, 90, 0.76);
border-radius: 14px;
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

button{
  background: #1C253C;
border-radius: 11px;
border-color: #1C253C;
width: 234px;
margin-top: 22px;
cursor: pointer;
outline: none;
height: 47px;
font-family: Open Sans;
font-style: normal;
font-weight: normal;
color: #ffffff;
font-size: 17px;
line-height: 23px;
}

#content-container{
  /* padding-top: 20px; */
  color: white;
  height: 500px;
  font-family: 'Open Sans';
  width: 760px;
  margin: 0 auto;
  margin-top:40px

}
p{
  padding-top: 9px;
}

.content{
  padding-left:20px;
}
.content:hover{
  cursor: pointer;
  /* background-color:	#3c1c31; */
  background: rgba(31, 62, 90, 0.76);
}

.delay-2nd{
  animation-delay: 4.5s;
}
.delay-3rd{
  animation-delay: 5s
}
.delay-4th{
  animation-delay: 5.5s
}

.delay-5th{
  animation-delay: 6s;
}

</style>
