<template>
  <div id="app">
    <header>
      <img class= "animated fadeInUp delay-1s" src="./assets/cross.svg"/>
      <h1 class="animated fadeInUp delay-2s">TH 151 Finals</h1>
      <h1 class="animated fadeInUp delay-2s">Cobbie's Catholic Creed</h1>
      <button @click="showExp" class="animated flipInX delay-3s">Show explanations</button>
      <p class="animated flipInX delay-3s" id="note">You can also hover over each line in the creed to toggle the explanations.</p>
    </header>
    <!-- <div id="cross-container"></div> -->

  <div id="content-container">
    <!-- First paragraph -->
    <p class="content animated fadeInLeftBig delay-4s">
      <mark id="first-par">I believe in the God of Jesus of Nazareth: <br />
      a God of mystery and love, <br />
      a God present in but beyond the Church, <br />
      whom we cannot and will not ever fully understand. </mark><br />
</p>
    <p v-if="visible===true" class="explanation animated zoomIn">Nam gravida eu mi sit amet viverra. Nam ut libero quis ligula eleifend egestas. In posuere, massa at cursus blandit, libero quam lobortis lorem, a egestas arcu ex vitae ipsum. Vestibulum auctor placerat lorem et scelerisque. Praesent non tincidunt sem.</p>

    <!-- Second paragraph -->
    <p class="content animated fadeInRightBig delay-2nd">
     <mark id="second-par"> I believe in the message and revelation of Jesus Christ, <br />
which is to bring God’s kingdom on Earth by taking the view of the victims.</mark><br>
</p>
    <p v-if="visible===true" class="explanation animated zoomIn">Nam gravida eu mi sit amet viverra. Nam ut libero quis ligula eleifend egestas. In posuere, massa at cursus blandit, libero quam lobortis lorem, a egestas arcu ex vitae ipsum. Vestibulum auctor placerat lorem et scelerisque. Praesent non tincidunt sem.</p>

    <!-- Third paragraph -->
    <p class="content animated fadeInLeftBig delay-3rd">
      <mark id="third-par">In the face of innocent suffering and vast injustice here on Earth, <br />
I believe in God’s gratuitous and divine love, <br />
for which we call Grace. </mark><br />
</p>
    <p v-if="visible===true" class="explanation animated zoomIn">Nam gravida eu mi sit amet viverra. Nam ut libero quis ligula eleifend egestas. In posuere, massa at cursus blandit, libero quam lobortis lorem, a egestas arcu ex vitae ipsum. Vestibulum auctor placerat lorem et scelerisque. Praesent non tincidunt sem.</p>


     <!--Fourth paragraph -->
    <p class="content animated fadeInRightBig delay-4th">
      <mark id="fourth-par">We cannot make God fit into our world and we cannot define God in our language; <br />
but we can discover God through understanding Grace. </mark><br />

    </p>
        <p v-if="visible===true" class="explanation animated zoomIn">Nam gravida eu mi sit amet viverra. Nam ut libero quis ligula eleifend egestas. In posuere, massa at cursus blandit, libero quam lobortis lorem, a egestas arcu ex vitae ipsum. Vestibulum auctor placerat lorem et scelerisque. Praesent non tincidunt sem.</p>


    <!-- Fifth paragraph-->
    <p class="content animated fadeInLeftBig delay-5th">
      <mark id="fifth-par">As Catholics, we believe in scripture, in saints, in Mary, and many other symbols and teachings unique to our faith. <br />
 but these all come second to what defines us as a follower of Jesus and a person of God, <br>
which is to make Jesus’ mission our own and translate this to action. </mark><br>

    </p>
        <p v-if="visible===true" class="explanation animated zoomIn">Nam gravida eu mi sit amet viverra. Nam ut libero quis ligula eleifend egestas. In posuere, massa at cursus blandit, libero quam lobortis lorem, a egestas arcu ex vitae ipsum. Vestibulum auctor placerat lorem et scelerisque. Praesent non tincidunt sem.</p>

  </div>
  </div>
  
    
</template>

<script>
export default {
  name: 'app',
  methods: {
    showExp: function(){
      this.visible = !this.visible;
      document.getElementsByClassName("content").classList.remove("animated")

    }
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      visible: false,
      styleObject: {
        'background-color': 'rgba(31, 62, 90, 0.76)',
      }
    }
  }
}
</script>

<style> 
body{
  /* background-color:#1c253c; */
  background-color:black;
  height: 120%;
}
mark{
  background-color: rgba(31, 62, 90, 0.76);
  color: white;
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
margin-top: 20px;
padding-left:20px;
padding-right: 20px;
background: rgba(31, 62, 90, 0.76);
border-radius: 14px;
font-style: italic
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
  /* background: rgba(31, 62, 90, 0.76); */
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

#first-par{
  background-color: rgba(31, 62, 90, 0.76)
}

#second-par{
  background: rgba(20, 80, 81, 0.76);
}

#third-par{
  background: rgba(40, 28, 60, 0.76);
}

#fourth-par{
background: rgba(60, 28, 49, 0.76);}

#fifth-par{
background: rgba(28, 37, 60, 0.76);}

</style>
