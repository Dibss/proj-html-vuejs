<template>
  <div class="presentation-container">
    <div class="presentation-container__left col-6">
      <h2 class="text-uppercase ls-2">presentation</h2>
      <div class="text-center p-relative">
        <img src="../../assets/img/461365506.webp" alt="">
        <div class="d-flex play-bar">
          <i class="fa-solid fa-play col-1 text-center" id="play" @click="pause()"></i>
          <i class="fa-solid fa-pause col-1 text-center d-none" id="pause" @click="play()"></i>
          <div class="progress-bar col-8 text-center"></div>
          <i class="fa-solid fa-signal col-1 text-center"></i>
          <i class="fa-solid fa-gear col-1 text-center"></i>
          <i class="fa-brands fa-vimeo-v col-1 text-center"></i>
        </div>
      </div>
    </div>
    <div class="presentation-container__right col-6">
      <h2 class="text-uppercase ls-2">twitter feed</h2>
      <ul>
        <li class="d-flex mb-4">
          <div class="col-1">
            <i class="fa-brands fa-twitter"></i>
          </div>
          <div class="col-11 t-gray fs-2">
            Stand out and be vibrant with some of the best bright and bold templates on <span class="t-scarlet">@Envato</span> Elements. And add a splash of c... <span><a href="https://t.co/jFrsnzEJK7" class="t-scarlet">https://t.co/jFrsnzEJK7</a></span>
            <span class="d-block fst-italic mt-2">3 days ago</span>
          </div>
        </li>
        <li class="d-flex mb-4">
          <div class="col-1">
            <i class="fa-brands fa-twitter"></i>
          </div>
          <div class="col-11 t-gray fs-2">
            Do you need to deliver the perfect presentation or creative pitch? Sure, your ideas and plan need to be on-point, b...<span><a href="https://t.co/nCmvsJVDpW" class="t-scarlet">https://t.co/nCmvsJVDpW</a></span>
            <span class="d-block fst-italic mt-2">9 days ago</span>
          </div>
        </li>
        <li class="d-flex mb-4">
          <div class="col-1">
            <i class="fa-brands fa-twitter"></i>
          </div>
          <div class="col-11 t-gray fs-2">
            Cut yourself a piece of the BFCM sales pie with a solid marketing plan. Here are 5 ways to optimize your content fo...<span><a href="https://t.co/UZfKHshEOT" class="t-scarlet">https://t.co/UZfKHshEOT</a></span>
            <span class="d-block fst-italic mt-2">11 days ago</span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
name: 'PresentationTwitterFeedComp',
methods : {
  play : function(){
    document.querySelector("#play").classList.remove("d-none")
    document.querySelector("#pause").classList.add("d-none")
  },
  pause : function(){
    document.querySelector("#play").classList.add("d-none")
    document.querySelector("#pause").classList.remove("d-none")
  }
}
}
</script>

<style scoped lang='scss'>
.presentation-container{
  width: 70%;
  margin: 2em auto;
  display: flex;
  flex-wrap: wrap;
  h2{
    margin-bottom: 1em;
  }
  &__left{
    img{
      max-width: 100%;
      height: auto;
      width: 80%;
    }
    .play-bar{
      background-color: rgba($color: #000000, $alpha: 0.8);
      padding: 0.6em 0;
      width: 95%;
      margin: 0 auto;
      position: absolute;
      bottom: 10px;
      .fa-brands,
      .fa-solid{
        color: #fff;
        cursor: pointer;
      }
      .progress-bar{
        border: 1px solid #868686;
      }
    }
  }
  &__right{
    .fa-brands{
      color: #45bdee;
    }
  }
}
</style>