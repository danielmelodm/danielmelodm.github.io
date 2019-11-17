<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/css?family=Nunito&display=swap" rel="stylesheet">
    <HelloWorld msg="Daniel Melo"/>
    <div>Entrepreneur Developer</div>
    <div>Cuisinier Amateur</div>
    <div>Crypto Entusiast</div>
    <br/>
    <div class="profile-link">
      <small><a href="https://www.linkedin.com/in/danielmelodev/">LinkedIn</a></small>
    </div>
    <div>
      <small><a href="https://keybase.io/danielmelogpi">Keybase</a></small>
    </div>
    <div>
      <small><a :href="emailhref">{{email}}</a></small>
    </div>
    <div class="footer">
      <img src="weiner-dog.svg" class="dog" />
      <img src="basket.svg" :class='{"basket-ball": true, "basket-ball-rotate": rotate}' />
    </div>
    <div class="triangle"></div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data() {
    return {
      rotate: false,
      emailhref: 'mailto:danielmelo.dm.dev@gmail.com',
      email: 'danielmelo.dm.dev@gmail.com'
    }
  },
  mounted() {
    setTimeout(() => {
      this.rotate = true
    }, 2000)
  }
}
</script>

<style>
#app {
  font-family: 'Nunito', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30vh;
  overflow: hidden;
  height: 100%;
}
@keyframes spin {
  from {transform:rotate(0deg);}  
  to {transform:rotate(360deg);}
}
a {
  color: darkcyan;
  text-decoration: none;
  font-size: 0.7rem;
}
.footer {
  position: fixed;
}
.footer {
  width: 100%;
  position: fixed;
  bottom: 0px;
  left: 0px;
  display: flex;
  text-align: center;
  overflow: hidden;
  border-bottom: 4px solid #279261c9;
  justify-content: center;
  z-index: 100
}
.dog {
  width: 3em;
  position: relative;
  bottom: -10px;
}
.basket-ball {
  width: 0.8em;
  right: 2em;
  bottom: -18px;
  position: relative;
  left: 0em;
}
.profile-link {
  padding: 0.5em;
}
.triangle {
  display: block;
  position: absolute;
  top: 0px;
  left: 0px;
  border-left: 25vw solid #03a9f4a8;
  border-right: 00vh solid red;
  border-top: 50vh solid #ffffff;
  border-bottom: 50vh solid #ffffffff;
  box-sizing: border-box;
}
</style>
