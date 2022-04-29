<template>
  <div class="bg-lightgray">
    <div class="sponsor-container">
      <h2 class="text-uppercase ls-1">sponsors</h2>
      <span class="fs-2 d-block">Maecenas faucibus mollis interdum. Nullam id dolor id nibh ultricies vehicula ut id elit</span>
      <div>
        <ul class="d-flex my-4">
          <li v-for="sponsor in sponsors" :key="sponsor.id" class="col-2">
            <img :src="sponsor.img" :alt="sponsor.name">
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'SponsorComp',
data(){
  return{
    sponsors : [
      {
        name : "dropler",
        img : require("../../assets/img/banner-1.jpg")
      },
      {
        name : "link sys",
        img : require("../../assets/img/banner-2.jpg")
      },
      {
        name : "pointer co",
        img : require("../../assets/img/banner-3.jpg")
      },
      {
        name : "max star",
        img : require("../../assets/img/banner-4.jpg")
      },
      {
        name : "globe care",
        img : require("../../assets/img/banner-5.jpg")
      },
      {
        name : "the shield",
        img : require("../../assets/img/banner-6.jpg")
      },
    ]
  }
}
}
</script>

<style scoped lang='scss'>
.sponsor-container{
  text-align: center;
  width: 70%;
  margin: 0 auto;
  padding: 2em 0 1em;
  h2{
    margin-bottom: 0.5em;
  }
  span{
    display: block;
    width: 30%;
    margin: 0 auto;
    color: #868686;
  }
  img{
    max-width: 100%;
    height: auto;
    width: 80%;
  }
}
</style>