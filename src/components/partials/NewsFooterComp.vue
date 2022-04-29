<template>
  <div class="newsfooter-container">
    <h4 class="text-uppercase ls-1 fw-normal">recent news</h4>
    <div class="my-2">
      <ul>
        <li v-for="elm in news" :key="elm.id">
          <i class="fa-solid fa-angle-right mr-4 fs-1"></i>
          <a :href="elm.url" class="fw-light text-uppercase">{{elm.title}}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
name: 'NewsFooterComp',
data(){
  return{
    news : [
      {
        title : "sem porta mollis parturient",
        url : "#"
      },
      {
        title : "nullam lorem mattis purus",
        url : "#"
      },
      {
        title : "nibh sem sit ullamcorper",
        url : "#"
      },
      {
        title : "donec luctus imperdiet",
        url : "#"
      },
      {
        title : "magna pars studiorum",
        url : "#"
      }
    ]
  }
}
}
</script>

<style scoped lang='scss'>
.newsfooter-container{
  color: #fff;
  li{
    color : #868686;
    a{
      color: #868686;
      font-size: 0.8rem;
    }
  }
}
</style>