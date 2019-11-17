<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/css?family=Nunito&display=swap" rel="stylesheet">
    <HelloWorld msg="Daniel Melo"/>
    <div>Entrepreneur Developer</div>
    <div>Cook</div>
    <div>Crypto Entusiast</div>
    <br/>
    <div class="profile-link">
      <small><a href="https://www.linkedin.com/in/danielmelodev/">LinkedIn</a></small>
    </div>
    <div>
      <small><a href="https://keybase.io/danielmelogpi">Keybase</a></small>
    </div>
    <img src="weiner-dog.svg" class="dog" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
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
  margin-top: 35vh;

}
a {
  color: darkcyan;
  text-decoration: none;
}
.dog {
  width: 3em;
  position: absolute;
  bottom: 1em;
}
.profile-link {
  padding: 0.5em;
}
</style>
