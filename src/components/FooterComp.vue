<template>
  <div class="bg-mineshaft">
    <div class="d-flex flex-wrap footer-container">
      <div class="col-3">
        <AboutUsComp/>
      </div>
      <div class="col-3">
        <NewsFooterComp/>
      </div>
      <div class="col-3">
        <TicketsFooterComp/>
      </div>
      <div class="col-3">
        <GalleryFooterComp/>
      </div>
    </div>
  </div>
</template>

<script>
import AboutUsComp from "./partials/AboutUsComp.vue";
import NewsFooterComp from "./partials/NewsFooterComp.vue";
import TicketsFooterComp from "./partials/TicketsFooterComp.vue";
import GalleryFooterComp from "./partials/GalleryFooterComp.vue";

export default {
name: 'FooterComp',
components: {
  AboutUsComp,
  NewsFooterComp,
  TicketsFooterComp,
  GalleryFooterComp
}
}
</script>

<style scoped lang='scss'>
.footer-container{
  width: 80%;
  margin: 0 auto;
  padding: 2em 0;
}
</style>