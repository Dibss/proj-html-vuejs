<template>
  <div class="news-container">
    <div class="d-flex jc-between">
      <h2 class="text-uppercase ls-1 mb-4">recent news</h2>
      <span class="text-capitalize news-link"><a href="#">read all news</a></span>
    </div>
    <div class="news-container__news">
      <ul class="d-flex">
        <li v-for="elm in news" :key="elm.id" class="col-4 mr-2">
          <div class="news-hover">
            <img :src="elm.img" :alt="elm.title">
            <div class="news-hover__content">
              <span class="text-uppercase d-none"><i class="fa-solid fa-bullhorn"></i> sticky post</span>
            </div>
          </div>
          <div class="d-flex jc-between col-8 flex-wrap fst-italic date-comments">
            <span class="fs-2">{{elm.date}}</span>
            <span class="fs-2">/</span>
            <span class="fs-2">{{elm.comments}}</span>
          </div>
          <h3 class="text-uppercase ls-1 fs-4 mb-2">{{elm.title}}</h3>
          <span class="fs-2">{{elm.overview}}</span>
          <span class="d-block text-capitalize read-more mt-2"><a :href="elm.url">read more</a></span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
name: 'RecentNewsComp',
data(){
  return{
    news : [
      {
        img : require("../../assets/img/photodune-7770665-two-white-coffee-mug-with-diy-decoration-o.jpg"),
        date : "03 Dec 2013",
        comments : "0 Comments",
        title : "sedial eiusmod tempor",
        overview : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum, dolor sint! Quae, commodi. Dolor exercitationem reprehenderit odit...",
        url : "#"
      },
      {
        img : require("../../assets/img/photodune-8797753-multiethnic-people-with-startup-business-t.jpg"),
        date : "03 Dec 2013",
        comments : "2 Comments",
        title : "donec luctus imperdiet",
        overview : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum, dolor sint! Quae, commodi. Dolor exercitationem reprehenderit odit...",
        url : "#"
      },
      {
        img : require("../../assets/img/photodune-8522811-speaker-at-business-conference-and-present.jpg"),
        date : "03 Dec 2013",
        comments : "2 Comments",
        title : "magna pars studorium",
        overview : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum, dolor sint! Quae, commodi. Dolor exercitationem reprehenderit odit...",
        url : "#"
      },
    ]
  }
}
}
</script>

<style scoped lang='scss'>
.news-container{
  width: 70%;
  margin: 3em auto;
  .news-link{
    a{
    color: #f72b0c;
    font-family: 'Libre Bodoni', serif;
    font-size: 0.9rem;
    }
  }
  &__news{
    li{
      .news-hover{
        position: relative;
        img{
          max-width: 100%;
          height: auto;
          margin-bottom: 1em;
        }
        &__content{
          display: flex;
          justify-content: flex-end;
          align-items: flex-end;
          position: absolute;
          bottom: 0;
          right: 0;
          top: 0;
          left: 0;
        }
        :hover span{
          display: unset;
          background-color: rgba($color: #000000, $alpha: 0.9);
          padding: 1em;
          margin-bottom: 2em;
          color: #fff;
          font-size: 0.6rem;
          font-weight: 700;
          letter-spacing: 0.2em;
          cursor: pointer;
        }
      }
      .date-comments{
        font-family: 'Libre Bodoni', serif;
      }
      span{
        color: #868686;
      }
      .read-more{
        a{
          color: #f72b0c;
          font-family: 'Libre Bodoni', serif;
          font-size: 0.9rem;
        }
      }
    }
  }
}
</style>