<template>
  <div class="tickets-container py-4">
    <div class="text-center">
      <h2 class="text-uppercase ls-2 mb-2">tickets</h2>
      <div>
        <ul class="d-flex">
          <li v-for="pass in tickets" :key="pass.id" class="mr-2">
            <div class="bg-gray py-2 tickets-container__title">
              <h3 class="text-uppercase">{{pass.pass}}</h3>
              <span class="text-uppercase price">{{pass.price}}</span>
              <div class="text-capitalize ticket-offer">{{pass.offer}}</div>
            </div>
            <div class="bg-white tickets-container__includes">
              <ul>
                <li v-for="elm in pass.includes" :key="elm.id" class="includes text-capitalize">{{elm}}</li>
              </ul>
            </div>
            <div class="text-uppercase book-link"><a :href="pass.url">book now</a></div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'TicketComp',
data(){
  return{
    tickets : [
      {
        pass : "one day pass",
        price : "free",
        includes : [
          "one day access",
          "coffee break",
          "lunch(international buffet)",
          "document sheets",
          "50USD voucher for next event"
        ],
        url : "#"
      },
      {
        pass : "four day passes",
        price : "750.00 USD",
        offer : "featured!",
        includes : [
          "four day access",
          "coffee break",
          "lunch(international buffet)",
          "document sheets",
          "100USD voucher for next event"
        ],
        url : "#"
      },
      {
        pass : "tro day pass",
        price : "580.00 USD",
        includes : [
          "two day access",
          "coffee break",
          "lunch(international buffet)",
          "document sheets",
          "70USD voucher for next event"
        ],
        url : "#"
      }
    ]
  }
}
}
</script>

<style scoped lang='scss'>
.tickets-container{
  background-image: url("../../assets/img/ticket-bg.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  h2{
    color: #fff;
  }
  &__title{
    padding: 1.5em 0;
    position: relative;
    .price{
      color: #f72b0c;
      font-weight: 700;
    }
  }
  &__includes{
    padding: 1em 0;
    .includes{
      font-family: 'Libre Bodoni', serif;
      color: #868686;
      padding: 0.5em 2em;
      font-size: 0.9rem;
    }
  }
  .ticket-offer{
    background-color: #f72b0c;
    position: absolute;
    color: white;
    font-family: 'Libre Bodoni', serif;
    top: 20px;
    right: -5px;
    transform: rotate(45deg);
    -webkit-transform: rotate(45deg);
  }
  .book-link{
    background-color: #f72b0c;
    padding: 0.8em 0;
    a{
      color: #fff;
      font-size: 0.9rem;
      font-weight: 700;
    }
  }
}
</style>