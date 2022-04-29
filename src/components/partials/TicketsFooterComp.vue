<template>
  <div class="ticket-footer">
    <h4 class="text-uppercase ls-1 fw-normal">get your seat!</h4>
    <span class="d-block my-2 fw-light fs-3 pr-2">Book for your seat before it's too late. We provide variety of ticket options</span>
    <div class="mt-4">
      <span class="text-uppercase fw-bold check-tickets fs-2"><a href="#">check out tickets!</a></span>
    </div>
  </div>
</template>

<script>
export default {
name: 'TicketsFooterComp',
}
</script>

<style scoped lang='scss'>
.ticket-footer{
  color: #fff;
  .check-tickets{
    padding: 1em;
    background-color: #f72b0c;
    a{
      color: #fff;
    }
  }
}
</style>