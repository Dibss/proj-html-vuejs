<template>
  <div id="app">
    <header>
      <HeaderComp/>
    </header>
    <main>
      <MainComp/>
    </main>
  </div>
</template>

<script>
import HeaderComp from "./components/HeaderComp.vue";
import MainComp from "./components/MainComp.vue";

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp
}
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Libre+Bodoni:ital@1&family=Roboto:ital,wght@0,300;0,400;0,700;1,300;1,400&display=swap');

*{padding: 0; margin: 0; box-sizing: border-box;}

#app{
  font-family: 'Roboto', sans-serif;
}

li{list-style-type: none;}
a{text-decoration: none;}

.d-block{display: block;}
.d-none{display: none;}

.d-flex{display: flex;}
.row{display: flex; flex-wrap: nowrap;}
.jc-between{justify-content: space-between;}
.ai-center{align-items: center;}
.flex-wrap{flex-wrap: wrap;}
.flex-column{flex-direction: column;}

.text-uppercase{text-transform: uppercase;}
.text-capitalize{text-transform: capitalize;}
.text-center{text-align: center;}
.fst-italic{font-style: italic;}
.fw-bold{font-weight: 700;}
.fw-light{font-weight: 300;}
.fs-6{font-size: 3rem;}
.fs-8{font-size: 4rem;}

.mr-1{margin-right: 0.5em;}
.mr-2{margin-right: 1em;}
.mt-3{margin-top: 1.5em;}
.my-4{margin: 2em 0;}
.mx-2{margin: 0 1em;}

.bg-lightgray{background-color: #f3f3f3;}
// for
@for $i from 1 through 12 {
    .col-#{$i}{-ms-flex-preferred-size: calc(100% / 12) * $i; max-width: calc(100% / 12) * $i; flex-basis: calc(100% / 12) * $i;}
}

@for $i from 1 through 12 {
    .offleft-#{$i}{margin-left: calc(100% / 12) * $i;}
}

@for $i from 1 through 12 {
    .offright-#{$i}{margin-left: calc(100% / 12) * $i;}
}

// variables
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
