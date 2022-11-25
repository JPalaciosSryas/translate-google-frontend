<template>
  <div id="app">
    <div class="nav">
      <NavigationBar />
      <div class="navInside">
        <div class="navInside-btns">
          <button class="navInside-btn"><router-link to="/">Text</router-link></button>
          <button class="navInside-btn"><router-link to="/about">Documents</router-link></button>
        </div>
        <div class="view">
          <router-view/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NavigationBar from '@/components/NavigationBar.vue';

export default {
  name: 'App',
  components: {
    NavigationBar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');

* {
   margin: 0px;
   padding: 0px;
}

#app {
  box-sizing: border-box;
  top: 0;
  width: 1350px;
  margin: 0;
  padding: 0;
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.nav {
  width: inherit;
  margin: 0 auto;
  padding: 0;
  position: absolute;
  z-index: 5;
}

.navInside {
  margin: 0;
  display: flex;
  justify-content: flex-start;
  height: 108px;
  background-color: #efefef;
  border-bottom: 1px solid #bbb;
}

.navInside-btns {
  margin: 0;
  position: absolute;
  z-index: 2;
  margin-left: 27px;
}

.navInside-btn {
  width: fit-content;
  height: fit-content;
  margin-top: 18px;
  margin-left: 9px;
  border: 1px solid #bbb;
  border-radius: 4px;
  padding: 9px 23px;
}

.navInside-btn a {
  font-weight: bold;
  color: #1a73e8;
  text-decoration: none;
}

.navInside-btn a.router-link-exact-active {
  color: #1a73e8;
}

.view {
  margin: 72px auto 0;
  width: 1332px;
  position: absolute;
  z-index: 0;
}
</style>
