<template>
  <div class="bg-lightgray">
    <div id="speakers-container">
      <div class="row jc-between my-4">
        <h2 class="text-uppercase">speakers</h2>
        <div>
          <span @click="prev()"><i class="fa-solid fa-angle-left"></i></span>
          <span @click="next()"><i class="fa-solid fa-angle-right"></i></span>
        </div>
      </div>
      <div>
        <ul class="row">
          <li class="speaker-card mr-4">
            <div class="speaker-hover">
              <img :src="speakers[currentIndex].img" :alt="speakers[currentIndex].name">
              <div class="img-mask">
                <a :href="speakers[currentIndex].twitter" class="d-none"><i class="fa-brands fa-twitter"></i></a>
                <a :href="speakers[currentIndex].facebook" class="mx-2 d-none"><i class="fa-brands fa-facebook-f"></i></a>
                <a :href="speakers[currentIndex].linkedin" class="d-none"><i class="fa-brands fa-linkedin-in"></i></a>
              </div>
            </div>
            <div class="text-center">
              <h4 class="text-uppercase">{{speakers[currentIndex].name}}</h4>
              <span class="fst-italic role">{{speakers[currentIndex].role}}</span>
            </div>
          </li>
          <li class="speaker-card mr-4">
            <div class="speaker-hover">
              <img :src="speakers[currentIndex + 1].img" :alt="speakers[currentIndex + 1].name">
              <div class="img-mask">
                <a :href="speakers[currentIndex + 1].twitter" class="d-none"><i class="fa-brands fa-twitter"></i></a>
                <a :href="speakers[currentIndex + 1].facebook" class="mx-2 d-none"><i class="fa-brands fa-facebook-f"></i></a>
                <a :href="speakers[currentIndex + 1].linkedin" class="d-none"><i class="fa-brands fa-linkedin-in"></i></a>
              </div>
            </div>
            <div class="text-center">
              <h4 class="text-uppercase">{{speakers[currentIndex + 1].name}}</h4>
              <span class="fst-italic role">{{speakers[currentIndex + 1].role}}</span>
            </div>
          </li>
          <li class="speaker-card mr-4">
            <div class="speaker-hover">
              <img :src="speakers[currentIndex + 2].img" :alt="speakers[currentIndex + 2].name">
              <div class="img-mask">
                <a :href="speakers[currentIndex + 2].twitter" class="d-none"><i class="fa-brands fa-twitter"></i></a>
                <a :href="speakers[currentIndex + 2].facebook" class="mx-2 d-none"><i class="fa-brands fa-facebook-f"></i></a>
                <a :href="speakers[currentIndex + 2].linkedin" class="d-none"><i class="fa-brands fa-linkedin-in"></i></a>
              </div>
            </div>
            <div class="text-center">
              <h4 class="text-uppercase">{{speakers[currentIndex + 2].name}}</h4>
              <span class="fst-italic role">{{speakers[currentIndex + 2].role}}</span>
            </div>
          </li>
          <li class="speaker-card mr-4">
            <div class="speaker-hover">
              <img :src="speakers[currentIndex + 3].img" :alt="speakers[currentIndex + 3].name">
              <div class="img-mask">
                <a :href="speakers[currentIndex + 3].twitter" class="d-none"><i class="fa-brands fa-twitter"></i></a>
                <a :href="speakers[currentIndex + 3].facebook" class="mx-2 d-none"><i class="fa-brands fa-facebook-f"></i></a>
                <a :href="speakers[currentIndex + 3].linkedin" class="d-none"><i class="fa-brands fa-linkedin-in"></i></a>
              </div>
            </div>
            <div class="text-center">
              <h4 class="text-uppercase">{{speakers[currentIndex + 3].name}}</h4>
              <span class="fst-italic role">{{speakers[currentIndex + 3].role}}</span>
            </div>
          </li>        
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'SpeakersComp',
data(){
  return{
    speakers : [
      {
        name : "patrick spencer",
        img : require("../../assets/img/speaker-6.jpg"),
        role : "S&P Analyzer",
        twitter : "#",
        facebook : "#",
        linkedin : "#"
      },
      {
        name : "janet jones",
        img : require("../../assets/img/speaker-5.jpg"),
        role : "Newyork Post's GM",
        twitter : "#",
        facebook : "#",
        linkedin : "#"
      },
      {
        name : "michael dover",
        img : require("../../assets/img/speaker-4.jpg"),
        role : "Starbuck's CEO",
        twitter : "#",
        facebook : "#",
        linkedin : "#"
      },
      {
        name : "angelina holy",
        img : require("../../assets/img/speaker-3.jpg"),
        role : "Maxii's Manager",
        twitter : "#",
        facebook : "#",
        linkedin : "#"
      },
      {
        name : "giorgio vanni",
        img : require("../../assets/img/speaker-2.jpg"),
        role : "Dragon Ball",
        twitter : "#",
        facebook : "#",
        linkedin : "#"
      },
      {
        name : "gianfranco crollo",
        img : require("../../assets/img/speaker-1.jpg"),
        role : "Model",
        twitter : "#",
        facebook : "#",
        linkedin : "#"
      },
      {
        name : "matteo matita",
        img : require("../../assets/img/speaker-7.jpg"),
        role : "Front-end Developer",
        twitter : "#",
        facebook : "#",
        linkedin : "#"
      },
      {
        name : "giulia comodino",
        img : require("../../assets/img/speaker-8.jpg"),
        role : "Poltrone & Poltrone",
        twitter : "#",
        facebook : "#",
        linkedin : "#"
      },
    ],
    currentIndex: 0
  }
},
methods: {
  next: function() {
    if (this.currentIndex < this.speakers.length - 1){
      this.currentIndex += 1;
    } else {
      this.currentIndex = 0;
    }
    console.log(this.currentIndex)
  },

  prev: function() {
    if(this.currentIndex == 0){
      this.currentIndex = this.speakers.length - 1;
    } else {
      this.currentIndex -= 1;
    }
    console.log(this.currentIndex)
  },
},
mounted(){
  console.log(this.currentIndex)
}
}
</script>

<style scoped lang='scss'>
#speakers-container{
  width: 70%;
  margin: 0 auto;
  padding: 2em 0 3em;
  h2{
    letter-spacing: 0.1em;
  }
  .fa-solid{
    color: #fff;
    background-color: #f72b0c;
    padding: 0.3em 0.6em;
    font-size: 0.8rem;
    margin-left: 0.2em;
    cursor: pointer;
  }
  .speaker-card{
    h4{
      letter-spacing: 0.1em;
    }
    img{
      max-width: 100%;
      height: auto;
    }
    .role{
      font-family: 'Libre Bodoni', serif;
      font-size: 0.9rem;
      color: #5d5d5c;
    }
    .speaker-hover{
      position: relative;
      img{
        border-radius: 5px;
      }
    }
  }
}

.speaker-hover:hover .img-mask{
  position: absolute;
  top : 0;
  bottom: 0;
  right: 0;
  left: 0;
  background-color: rgba($color: #f72b0c, $alpha: 0.5);
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
  .fa-brands{
    color: #fff;
    cursor: pointer;
  }
}
.speaker-hover:hover .img-mask a{display: unset;}
</style>