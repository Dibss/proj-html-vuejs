<template>
  <div class="aboutus-container">
    <h4 class="text-uppercase ls-1 fw-normal">about us</h4>
    <span class="d-block my-2 fw-light fs-3">Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.</span>
    <div>
      <ul class="d-flex">
        <li>
          <a href="#"><i class='fa-brands fa-facebook-square'></i></a>
        </li>
        <li>
          <a href="#"><i class='fa-brands fa-twitter-square'></i></a>
        </li>
        <li>
          <a href="#"><i class="fa-brands fa-linkedin"></i></a>
        </li>
        <li>
          <a href="#"><i class='fa-brands fa-google-plus-square'></i></a>
        </li>
        <li>
          <a href="#"><i class='fa-brands fa-pinterest-square'></i></a>
        </li>
        <li>
          <a href="#"><i class='fa-solid fa-bars'></i></a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
name: 'AboutUsComp',
}
</script>

<style scoped lang='scss'>
.aboutus-container{
  color: #fff;
  a{
    color: #fff;
    margin-right: 1em;
  }
}
</style>