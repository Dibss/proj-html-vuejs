<template>
  <div>
    <div class="map">
      <div class="map-satellite">
        <span>Map</span>
        <span class="t-gray">Satellite</span>
      </div>
      <div class="marker">
        <img src="../../assets/img/default_marker.png" alt="location marker">
      </div>
      <div class="user-marker">
        <img src="../../assets/img/image (4).svg" alt="location marker" draggable="true" id="marker-release" @click="markerClick()">
        <img src="../../assets/img/image (6).svg" alt="location marker" class="d-none" id="marker-click" @click="markerRelease()">
      </div>
      <div class="zoom">
        <div><i class="fa-solid fa-plus"></i></div>
        <div><i class="fa-solid fa-minus"></i></div>
      </div>
    </div>
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
          <span class="fs-2"><i class="fa-solid fa-phone"></i> +1-112-222-3344</span>
          <span class="fs-2"><i class="fa-solid fa-envelope"></i>Contact@TheKeyNoteTheme.com</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'LocationComp',
methods : {
  markerClick(){
    document.querySelector("#marker-click").classList.remove("d-none")
    document.querySelector("#marker-release").classList.add("d-none")
  },
  markerRelease(){
    document.querySelector("#marker-click").classList.add("d-none")
    document.querySelector("#marker-release").classList.remove("d-none")
  }
}
}
</script>

<style scoped lang='scss'>
.map{
  height: 50vh;
  background-image: url("../../assets/img/map.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  position: relative;
  .map-satellite{
    position: absolute;
    top: 15px;
    left: 15px;
    span{
      background-color: #fff;
      padding: 0.5em 1em;
      border: 1px solid #868686;
      font-size: 0.9rem;
      cursor: pointer;
    }
  }
  .marker{
    position: absolute;
    top: 46%;
    left: 50%;
    transform: translate(50%,-50%);
  }
  .user-marker{
    position: absolute;
    right: 10px;
    bottom: 30%;
    background-color: #fff;
    padding: 0.5em 0.3em 0.3em 0.6em;
    img{
      max-width: 100%;
      height: auto;
      width: 80%;
      cursor: pointer;
    }
  }
  .zoom{
    position: absolute;
    right: 10px;
    bottom: 10%;
    div i{
      background-color: #fff;
      padding: 1em 1em;
      border: 1px solid #868686;
      font-size: 0.8rem;
      cursor: pointer;
    }
  }
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