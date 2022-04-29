<template>
  <div class="gallery-footer">
    <h4 class="text-uppercase ls-1 fw-normal">gallery from last year</h4>
    <div>
      <ul class="row-wrap">
        <li v-for="img in gallery" :key="img.id" class="col-3 p-1">
          <img :src="img">
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
name: 'GalleryFooterComp',
data(){
  return{
    gallery : [
      require("../../assets/img/photodune-7770665-two-white-coffee-mug-with-diy-decoration-o (1).jpg"),
      require("../../assets/img/photodune-8523683-speaker-at-business-convention-and-present.jpg"),
      require("../../assets/img/photodune-6745579-modern-creative-man-relaxing-on-workspace-.jpg"),
      require("../../assets/img/photodune-8522811-speaker-at-business-conference-and-present (1).jpg"),
      require("../../assets/img/photodune-8797753-multiethnic-people-with-startup-business-t (1).jpg"),
      require("../../assets/img/card04-150x150.jpg"),
      require("../../assets/img/photodune-6745606-man-wristwatch-calendar-key-and-glasses-on.jpg"),
      require("../../assets/img/photodune-6745585-modern-creative-workspace-m-150x150.jpg"),
      require("../../assets/img/6426608875_186070f8ca_o-150x150.jpg"),
      require("../../assets/img/card01-150x150.jpg"),
      require("../../assets/img/13349065283_64d09b067c_o-150x150.jpg"),
      require("../../assets/img/photodune-8795110-overhead-of-essentials-denim-clothes-m-150.jpg"),
    ]
  }
}
}
</script>

<style scoped lang='scss'>
.gallery-footer{
  color: #fff;
  h4{
    margin-bottom: 1em;
  }
  img{
    max-width: 100%;
    height: auto;
  }
}
</style>