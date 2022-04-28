<template>
  <div id="info-container">
    <div class="row info-content">
      <div class="col-4 d-flex">
        <div class="col-2 text-center"><i class="fa-solid fa-trophy"></i></div>
        <div class="col-10">
          <h2>who we are</h2>
          <span>Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.</span>
          <div class="learn">
            <a href="#" class="fst-italic text-capitalize">learn more</a>
          </div>
        </div>
      </div>
      <div class="col-4 d-flex">
        <div class="col-2 text-center"><i class="fa-solid fa-bolt-lightning"></i></div>
        <div class="col-10">
          <h2>what we do</h2>
          <span>Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.</span>
          <div class="learn">
            <a href="#" class="fst-italic text-capitalize">learn more</a>
          </div>
        </div>
      </div>
      <div class="col-4 d-flex">
        <div class="col-2 text-center"><i class="fa-solid fa-question"></i></div>
        <div class="col-10">
          <h2>why us?</h2>
          <span>Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.</span>
          <div class="learn">
            <a href="#" class="fst-italic text-capitalize">learn more</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'InfoComp',
}
</script>

<style scoped lang='scss'>
#info-container{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 75%;
  margin: 4em auto;
  .info-content{
    justify-content: space-between;
    align-items: center;
    .fa-solid{
      color: #868686;
      font-size: 1.5em;
    }
    h2{
      text-transform: uppercase;
      color: #272727;
      font-size: 1.1rem;
      margin-bottom: 1em;
    }
    span{
      color: #868686;
      font-size: 0.9rem;
    }
    .learn{
      margin-top: 1em;
      a{
        color: #f72b0c;
        font-family: 'Libre Bodoni', serif;
      }
    }
  }
}
</style>