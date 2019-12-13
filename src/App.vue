<template>
  <div id="app">
    <header>
      <img :class="['animated', {'fadeInUp': isNotDone, 'delay-1s': isNotDone, 'pulse': !isNotDone, 'infinite': !isNotDone}]" src="./assets/cross.svg"/>
      <h1 class="animated fadeInUp delay-2s">TH 151 Finals</h1>
      <h1 class="animated fadeInUp delay-2s">Cobbie's Catholic Creed</h1>
      <button @click="showExp" class="animated flipInX delay-button">{{buttonText}} explanations</button>
      <p class="animated flipInX delay-button" id="note">Click on the button above to toggle the explanations per section of the Creed.</p>
    </header>
    <!-- <div id="cross-container"></div> -->

  <div id="content-container">
    <!-- First paragraph -->
    <p :class="[content, {'animated': isNotDone, 'fadeInLeftBig': isNotDone, 'delay-4s': isNotDone}]">
I believe in the God of Jesus of Nazareth: <br />
      a God of mystery and love, <br />
      a God present in but beyond the Church, <br />
      whom we cannot and will not ever fully understand. <br />
</p>
    <p v-if="visible===true" class="explanation animated zoomIn">
One of the most impactful things I learned this semester is that the God that has been taught to me - the God I grew up with and used to believe - is most likely nothing even close to depicting what God is actually like. While there are other things that remained true, such as God being a God of love, most of what we know about God has been limited to human interpretation.
      </p>

    <!-- Second paragraph -->
    <p :class="[content, {'animated': isNotDone, 'fadeInRightBig': isNotDone, 'delay-2nd': isNotDone}]">
I believe in the message and revelation of Jesus Christ, <br />
which is to bring God’s kingdom on Earth by taking the view of the victims.<br>
</p>
    <p v-if="visible===true" class="explanation explanation-2 animated zoomIn">
      We can speak of God through Jesus. We must acknowledge that Jesus was truly human - not someone like Thanos or Luke Skywalker, which is the image of most people - in order to acknowledge one of the central principles of Christianity, which is that God became man. Looking at Jesus’ life and the message he wanted to spread leads us to this view of the victims, which is also central to the Christian faith.
      </p>

    <!-- Third paragraph -->
    <p :class="[content, {'animated': isNotDone, 'fadeInLeftBig': isNotDone, 'delay-3rd': isNotDone}]">
In the face of innocent suffering and vast injustice here on Earth, <br />
I believe in God’s gratuitous and divine love, <br />
for which we call Grace. <br />
</p>
    <p v-if="visible===true" class="explanation explanation-3 animated zoomIn">
      One of the most important questions to ask about our faith is this: how can we speak meaningfully of God in the face of these evils? This leads us to understand that God’s unconditional and gratuitous love does not work within the reward-and-punishment frameworks and limitations of the human understanding of God.
      </p>


     <!--Fourth paragraph -->
    <p :class="[content, {'animated': isNotDone, 'fadeInRightBig': isNotDone, 'delay-4th': isNotDone}]">
We cannot make God fit into our world and we cannot define God in our language; <br />
but we can discover God through understanding Grace. <br />

    </p>
        <p v-if="visible===true" class="explanation explanation-4 animated zoomIn">
          Now connecting some of the previous concepts, although we can’t ever get close to truly defining God, that doesn’t mean that we should simply stop there. We can get to know God as best we can, within our human limitations, through Grace.
        </p>


    <!-- Fifth paragraph-->
    <p :class="[content, {'animated': isNotDone, 'fadeInLeftBig': isNotDone, 'delay-5th': isNotDone}]">
As Catholics, we believe in teachings from scripture, in saints and in Mary, in the sacraments, and in many other symbols and practices unique to our faith. <br />
But these all come second to what defines us as a follower of Jesus and a person of God, <br>
which is to make Jesus’ mission our own and translate this into action. <br>

    </p>
        <p v-if="visible===true" class="explanation explanation-5 animated zoomIn">
          Many Catholics treat integral beliefs and practices of the Christian faith as rituals, and don’t go beyond that. This even extends to gatekeeping, as we tend to define each other based on what rules they follow rather than their humanity. While believing and practicing certain things are important, we should always remember that what should be the essence of our Christian faith is to act upon the message and mission Jesus imparted to this world.
          </p>

  </div>
  </div>
  
    
</template>

<script>
export default {
  name: 'app',
  methods: {
    showExp: function(){
      this.visible = !this.visible;
      this.buttonText === 'Show' ? this.buttonText = 'Hide' : this.buttonText = 'Show'
    },
    removeAnimations: function(){
      // var contentList = document.getElementsByClassName("content");
        this.classList.remove('animated')
    }
  },
  
  beforeUpdate: function(){
    this.isNotDone =false
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      visible: false,
      styleObject: {
        'background-color': 'rgba(31, 62, 90, 0.76)',
      },
      isNotDone: true,
      content: 'content',
      buttonText: 'Show'
    }
  }
}
</script>

<style> 
@import url('https://fonts.googleapis.com/css?family=Merriweather|Open+Sans&display=swap');
body{
  /* background-color:#1c253c; */
  background-color:#949CA3;
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
  font-family: 'Open Sans',sans-serif;
font-style: italic;
font-size: 13px;
line-height: 15px;
color: #ffffff

}

.explanation{
  /* width: 807px; */
height: 100px;
margin-top: 20px;
padding-left:20px;
padding-right: 20px;
background: rgba(31, 62, 90, 0.76);
border-radius: 14px;
font-style: italic
}

.explanation-2{
  /* background: rgba(20, 80, 81, 0.76); */
  background: rgba(179,154,103, 0.76);
height: 120px;

}

.explanation-3{
  /* background: rgba(40, 28, 60, 0.76); */
  background: rgba(216,174,70, 0.76)


}

.explanation-4{
/* background: rgba(60, 28, 49, 0.76); */
background: rgba(178,76,46,0.76);
height: 80px;
}

.explanation-5{
background: rgb(51, 71, 98, 0.76);
height: 120px;

}

header{
  color: white;
  font-family: 'Merriweather',serif;
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
  /* background: #1C253C; */
  background: #334762;
border-radius: 11px;
border-color: #334762;
width: 234px;
margin-top: 22px;
cursor: pointer;
outline: none;
height: 47px;
font-family: 'Open Sans',sans-serif;
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
  font-family: 'Open Sans', sans-serif;
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

.delay-button{
    animation-delay: 3.65s;
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
  /* background: rgba(20, 80, 81, 0.76); */
  background: rgba(179,154,103, 0.76)
}

#third-par{
  /* background: rgba(40, 28, 60, 0.76); */
  background: rgba(216,174,70, 0.76)
}

#fourth-par{
/* background: rgba(60, 28, 49, 0.76); */
background: rgba(178,76,46,0.76)
}

#fifth-par{
/* background: rgba(28, 37, 60, 0.76); */
background: rgb(51, 71, 98, 0.76)
}
/* #1C253C */

</style>
