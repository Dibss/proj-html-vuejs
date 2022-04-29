<template>
  <div>
    <div class="map"></div>
    <div class="location-hero">
      <div class="col-12">
        <h3 class="text-uppercase">location</h3>
        <span class="text-uppercase d-block fw-bold ls-2">gd building, grand conference room</span>
        <span class="d-block fs-1 fw-light"><i class="fa-solid fa-location-arrow my-2"></i> 11 GD Building, River Mall, New York, USA 8879</span>
        <span class="text-capitalize fw-light fs-2"><a href="#">check for accomodations here</a></span>
      </div>
      <div class=location-hero__contacts>
        <hr>
        <div>
          <span class="fs-1"><i class="fa-solid fa-phone"></i> +1-112-222-3344</span>
          <span class="fs-1"><i class="fa-solid fa-envelope"></i>Contact@TheKeyNoteTheme.com</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'LocationComp',
}
</script>

<style scoped lang='scss'>
.map{
  height: 50vh;
  background-color: gray;
}
.location-hero{
  background-image: url("../../assets/img/location-bg.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 50vh;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  color: #fff;
  text-align: center;
  padding: 2em 0;
  h3{
    font-size: 1.5em;
    letter-spacing: 0.1em;
    margin-bottom: 1em;
  }
  a{
    color: #f72b0c;
  }
  &__contacts{
    width: 25%;
    margin: 0 auto;
    hr{
      margin-bottom: 0.5em;
      height: 2px;
      border-color: #fff;
      background-color: #fff;
    }
    div{
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      .fa-solid{
        margin-right: 0.5em;
      }
    }
  }
}
</style>