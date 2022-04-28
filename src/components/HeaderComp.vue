<template>
  <div>
    <NavComp/>
    <HeroComp/>
  </div>
</template>

<script>
import NavComp from "./partials/NavComp.vue";
import HeroComp from "./partials/HeroComp.vue";
export default {
    name: "HeaderComp",
    components: { NavComp, HeroComp }
}
</script>

<style scoped lang='scss'>
</style>