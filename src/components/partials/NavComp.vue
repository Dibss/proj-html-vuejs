<template>
  <nav>
    <div>
      <img src="../../assets/img/logo.png" alt="the keynote logo">
    </div>
    <div id="top-right">
      <ul>
        <li v-for="elm in topMenu" :key="elm.id" class="text-uppercase"><a :href="elm.url">{{elm.name}}</a></li>
      </ul>
      <div id="search">
        <input type="search">
      </div>
    </div>
  </nav>
</template>

<script>
export default {
name: 'NavComp',
data(){
  return{
    topMenu : [
      {
        name : "home",
        url : "#"
      },
      {
        name : "pages",
        url : "#"
      },
      {
        name : "program",
        url : "#"
      },
      {
        name : "tickets",
        url : "#"
      },
      {
        name : "speakers",
        url : "#"
      },
      {
        name : "papers",
        url : "#",
      },
      {
        name : "blog",
        url : "#",
      },
      {
        name : "shortcodes",
        url : "#"
      }
    ]
  }
}
}
</script>

<style scoped lang='scss'>
nav{
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 70%;
  margin: 0 auto;
  padding: 1em 0;
  #top-right{
    display: flex;
    align-items: center;
    ul{
      display: flex;
      align-items: center;
      li{
        margin-right: 1.5em;
        border-bottom: 3px solid transparent;
        :hover{
          color: #f72b0c;
          border-bottom: 3px solid #f72b0c;
        }
        a{
          color: #868686;
          font-weight: 700;
          padding-bottom: 0.5em;
        }
      }
    }

    #search{
      input[type=search] {
        text-align: right;
        outline: none;
        width: 15px;
        padding-left: 10px;
        color: transparent;
        cursor: pointer;
        background: #fff url(https://static.tumblr.com/ftv85bp/MIXmud4tx/search-icon.png) no-repeat 9px;
        padding: 9px 10px 9px 32px;
        
        -webkit-transition: all .5s;
        -moz-transition: all .5s;
        transition: all .5s;
        border: none;
        border-left: 1px solid #868686;
      }
      input[type=search]:focus{
        width: 150px;
        padding-right: 32px;
        color: #000;
        background-color: #fff;
        cursor: auto;
      }
    }
  }
}
</style>