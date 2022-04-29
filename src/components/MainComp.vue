<template>
  <div>
    <InfoComp/>
    <SubscribeComp/>
    <SpeakersComp/>
    <ProgramComp/>
    <RecentNewsComp/>
    <TicketsComp/>
    <PresentationTwitterFeedComp/>
    <SponsorComp/>
  </div>
</template>

<script>
import InfoComp from "./partials/InfoComp.vue";
import SubscribeComp from "./partials/SubscribeComp.vue";
import SpeakersComp from "./partials/SpeakersComp.vue";
import ProgramComp from "./partials/ProgramComp.vue";
import RecentNewsComp from "./partials/RecentNewsComp.vue";
import TicketsComp from "./partials/TicketsComp.vue";
import PresentationTwitterFeedComp from "./partials/PresentationTwitterFeedComp.vue";
import SponsorComp from "./partials/SponsorComp.vue";

export default {
name: 'MainComp',
components : {
    InfoComp,
    SubscribeComp,
    SpeakersComp,
    ProgramComp,
    RecentNewsComp,
    TicketsComp,
    PresentationTwitterFeedComp,
    SponsorComp
}
}
</script>

<style scoped lang='scss'>
</style>