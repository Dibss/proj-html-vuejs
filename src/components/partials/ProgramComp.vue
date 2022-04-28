<template>
  <div class="program-container">
    <div class="d-flex ai-center flex-wrap">
      <div class="program-container__title">
        <h2 class="text-uppercase">program</h2>
      </div>
      <div class="program-container__details">
        <span class="d-block">This conference run through all 4 days from 23 - 26 May 2016</span>
        <span class="d-block">We also provide free lunch and coffee break in each day</span>
      </div>
      <div class="program-container__link">
        <a href="#" class="text-capitalize">view full program</a>
      </div>
      <div class="program-container__program d-flex flex-wrap">
        <div class="program-days">
          <ul class="row">
            <li v-for="elm in program" :key="elm.id" class="col-2">
              <h3 class="text-uppercase">{{elm.day}}</h3>
              <span>{{elm.date}}</span>
            </li>
          </ul>
        </div>
        <div class="program-details row bg-lightgray">
          <div class="program-details__left mt-3">
            <div class="d-flex ai-center flex-wrap">
              <span class="col-12"><i class="fa-solid fa-clock mr-2"></i>{{program[0].schedule}}</span>
              <span class="col-12 text-uppercase"><i class="fa-solid fa-location-arrow mr-2"></i>{{program[0].location}}</span>
              <span class="col-12 text-uppercase speaker-of-day"><i class="fa-solid fa-user mr-2"></i>{{program[0].speaker}}</span>
            </div>
          </div>
          <div class="program-details__right">
            <h4 class="text-uppercase">{{program[0].title}}</h4>
            <span>{{program[0].description}}</span>
            <img :src="program[0].speakerImg" :alt="program[0].speaker">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'ProgramComp',
data(){
  return{
    program : [
      {
        day : "day 1",
        date : "23 May 2019",
        schedule : "09:00 - 10:30",
        location : "roma",
        speaker : "laurence francis",
        title : "welcoming and introduction",
        description : "Vestibulum ud ligula porta felis euismod semper. Nullarm quis risus eget urna mollis ornare vel eu leo. Donec ullamcorper nulla non metus auctor fringilla. Aenean lacinia bibendum nulla sed consectetur.",
        speakerImg : require("../../assets/img/speaker-8-150x150.jpg")
      },
      {
        day : "day 2",
        date : "24 May 2019",
        schedule : "09:00 - 10:30",
        location : "roma",
        speaker : "patrick spencer",
        title : "lorem ipsum",
        description : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis minus possimus recusandae est nihil velit voluptatem illo deserunt eligendi id qui eos dolore soluta repellendus quis, atque accusantium ipsum minima?",
        speakerImg : require("../../assets/img/speaker-6-150x150.jpg")
      },
      {
        day : "day 3",
        date : "25 May 2019",
        schedule : "09:00 - 10:30",
        location : "roma",
        speaker : "janet jones",
        title : "lorem ipsum",
        description : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis minus possimus recusandae est nihil velit voluptatem illo deserunt eligendi id qui eos dolore soluta repellendus quis, atque accusantium ipsum minima?",
        speakerImg : require("../../assets/img/speaker-5-150x150.jpg")
      },
      {
        day : "day 4",
        date : "26 May 2019",
        schedule : "09:00 - 10:30",
        location : "roma",
        speaker : "michael dover",
        title : "lorem ipsum",
        description : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis minus possimus recusandae est nihil velit voluptatem illo deserunt eligendi id qui eos dolore soluta repellendus quis, atque accusantium ipsum minima?",
        speakerImg : require("../../assets/img/speaker-4-150x150.jpg")
      },
      {
        day : "",
        date : "",
        schedule : "",
        location : "",
        speaker : "",
        title : "",
        description : "",
        speakerImg : ""
      },
      {
        day : "",
        date : "",
        schedule : "",
        location : "",
        speaker : "",
        title : "",
        description : "",
        speakerImg : ""
      },
    ]
  }
}
}
</script>

<style scoped lang='scss'>
.program-container{
  width: 70%;
  margin: 4em auto;
  &__title{
    flex-basis: 20%;
    letter-spacing: 0.2em;
  }
  &__details{
    flex-basis: 60%;
    font-size: 0.9rem;
    color: #868686;
  }
  &__link{
    flex-basis: 20%;
    text-align: right;
    a{
        color: #f72b0c;
        font-family: 'Libre Bodoni', serif;
        font-size: 0.9rem;
      }
  }
  &__program{
    margin: 3em 0;
    .program-days{
      flex-basis: 100%;
      li{
        background-color: #f72b0c;
        color: #fff;
        padding: 1em;
        border-right: 1px solid #bf351f;
        h3{font-size: 1rem;}
        span{font-size: 0.9rem;}
      }
      li:hover{background-color: #bf351f;}
    }
  }
}

.program-details{
  &__left{
    flex-basis: 30%;
    display: flex;
    margin-left: 3em;
    .speaker-of-day{color: #f72b0c;}
    .fa-solid{color: #868686;}
  }
  &__right{
    flex-basis: 70%;
  }
}
</style>