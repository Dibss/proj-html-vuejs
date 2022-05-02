<template>
  <div id="subscribe-hero">
    <div>
      <div id="countdown" class="row">
        <div class="mr-2">
          <div id="days" class="fs-6"></div>
          <span class="d-block text-uppercase fw-light">days</span>
        </div>
        <div class="mr-2">
          <div id="hours" class="fs-6"></div>
          <span class="d-block text-uppercase fw-light">hours</span>
        </div>
        <div class="mr-2">
          <div id="mins" class="fs-6"></div>
          <span class="d-block text-uppercase fw-light">mins</span>
        </div>
        <div>
          <div id="secs" class="fs-6"></div>
          <span class="d-block text-uppercase fw-light">secs</span>
        </div>
      </div>
      <div>
        <h3 class="text-uppercase my-4">subscribe for updates</h3>
        <form>
          <input type="email" placeholder="Please fill your email" v-model="email" required>
          <button type="submit" class="text-uppercase btn" @click.prevent="subscribe()" @keyup.enter="subscribe()">subscribe</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'SubscribeComp',
data(){
  return{
    email : ""
    }
},
created(){
  this.countdown()
},
methods : {
  countdown(){
    let countDownDate = new Date("Aug 18, 2031 15:37:25").getTime();
    setInterval(function(){
      let now = new Date().getTime();
      let distance = countDownDate - now;
      let days = Math.floor(distance / (1000 * 60 * 60 * 24));
      let hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      let seconds = Math.floor((distance % (1000 * 60)) / 1000);
      document.getElementById("days").innerHTML = days;
      document.getElementById("hours").innerHTML = hours;
      document.getElementById("mins").innerHTML = minutes;
      document.getElementById("secs").innerHTML = seconds;
      if (distance < 0) {
        clearInterval(this.countdown());
        document.getElementById("countdown").innerHTML = "EXPIRED";
      }
    }, 1000);
  },
  subscribe(){
    this.email = "";
  }
}
}
</script>

<style scoped lang='scss'>
#subscribe-hero{
  background-image: url(../../assets/img/coutdown-bg1.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 50vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  #countdown > div{
      background-color: rgba($color: #000000, $alpha: 0.7);
      color: #fff;
      font-weight: 700;
      padding: 1em 2em;
      span{font-size: 0.9rem;}
  }
  h3{
    letter-spacing: 0.2em;
  }
  form input{
    padding: 1em;
    margin-right: 1em;
  }
  .btn{
    background-color: #f72b0c;
    padding: 0.8em 1.5em;
    background-color: #f72b0c;
    padding: 1.1em 1.5em;
    border: none;
    border-radius: 5px;
    color: #fff;
  }
}
</style>