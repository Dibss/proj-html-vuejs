<template>
  <div class="program-container">
    <div class="row ai-center">
      <div class="program-container__title">
        <h2 class="text-uppercase">program</h2>
      </div>
      <div class="program-container__details">
        <span class="d-block">This conference run through all 4 days from 23 - 26 May 2016</span>
        <span class="d-block">We also provide free lunch and coffee break in each day</span>
      </div>
      <div class="program-container__program">
        <a href="#" class="text-capitalize">view full program</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'ProgramComp',
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
  &__program{
    flex-basis: 20%;
    text-align: right;
    a{
        color: #f72b0c;
        font-family: 'Libre Bodoni', serif;
        font-size: 0.9rem;
      }
  }
}
</style>