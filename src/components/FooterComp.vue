<template>
  <div class="bg-masala">
    <div class="d-flex flex-wrap footer-container">
      <div class="col-3">
        <AboutUsComp/>
      </div>
      <div class="col-3">

      </div>
      <div class="col-3">

      </div>
      <div class="col-3">

      </div>
    </div>
  </div>
</template>

<script>
import AboutUsComp from "./partials/AboutUsComp.vue"

export default {
name: 'FooterComp',
components: {
  AboutUsComp
}
}
</script>

<style scoped lang='scss'>
.footer-container{
  width: 70%;
  margin: 0 auto;
}
</style>