<template>
  <div>
    <InfoComp/>
    <SubscribeComp/>
    <SpeakersComp/>
    <ProgramComp/>
  </div>
</template>

<script>
import InfoComp from "./partials/InfoComp.vue";
import SubscribeComp from "./partials/SubscribeComp.vue";
import SpeakersComp from "./partials/SpeakersComp.vue";
import ProgramComp from "./partials/ProgramComp.vue";

export default {
name: 'MainComp',
components : {
    InfoComp,
    SubscribeComp,
    SpeakersComp,
    ProgramComp
}
}
</script>

<style scoped lang='scss'>
</style>