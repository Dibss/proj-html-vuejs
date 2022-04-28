<template>
  <div class="hero">
    <div>
      <span class="fw-light fs-6 d-block">conference on</span>
      <span class="fw-bold fs-8 social-net-span d-block">social networks</span>
      <div class="conference-details">
          <hr>
          <div>
            <span>23 - 26 may 2019</span>
            <span>/</span>
            <span>san francisco</span>
            <span>/</span>
            <span>8 speakers</span>
          </div>
      </div>
      <span class="register"><a href="#">register online</a></span>
    </div>
  </div>
</template>

<script>
export default {
name: 'HeroComp',
}
</script>

<style scoped lang='scss'>
.hero{
  background-image: url(../../assets/img/slider-1-bg.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 50vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  text-transform: uppercase;
  color: #fff;
  .social-net-span{
    margin: 0.2em 0 .4em;
  }
  .conference-details{
    width: 70%;
    margin: 0 auto 2.5em;
    hr{
      border-color: #fff;
      background-color: #fff;
      height: 3px;
      margin-bottom: 0.5em;
    }
    div{
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
    }
  }
  .register{
    padding: 0.8em 1.5em;
    background-color: #f72b0c;
    border-radius: 5px;
    a{color: #fff;}
  }
}
</style>