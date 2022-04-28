<template>
  <div id="app">
    <header>
      <HeaderComp/>
    </header>
  </div>
</template>

<script>
import HeaderComp from "./components/HeaderComp.vue";

export default {
  name: 'App',
  components: {
    HeaderComp
}
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');
*{padding: 0; margin: 0; box-sizing: border-box;}
#app{
  font-family: 'Roboto', sans-serif;
}

li{list-style-type: none;}
a{text-decoration: none;}

.d-block{display: block;}
.text-uppercase{text-transform: uppercase;}
.fw-bold{font-weight: 700;}
.fw-light{font-weight: 300;}
.fs-6{font-size: 3rem;}
.fs-8{font-size: 4rem;}

$white : #fff;
$mine-shaft : #272727;
$gray : #868686;
$scarlet : #f72b0c;
$cloud : #c6c1bd;
$froly : #f0776b;

$masala : #403d3b;
$dust-storm : #e4cdc9;
$natural-gray : #8b8a87;
$dusty-gray : #9c9c9c;
$sushi : #86b54a;

$sushi-vibrant : #86b648;
$chicago-muted : #5d5d5c;
$thunderbird-darkvibrant : #bf351f;
$black-darkmuted : #040404;
$burnt-sienna : #e97c62;
</style>
