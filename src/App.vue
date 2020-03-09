<template>
  <div class="app">
    <div class='navigation'>
        <router-link to="/bookmark1" class='navigation-box'>Закладка 1</router-link>
        <router-link to="/switch" class='navigation-box'>Switch</router-link>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
import Switch from './components/Switch.vue';
import Bookmark1 from './components/Bookmark1';
import Vue from 'vue';
import VueRouter from 'vue-router';

Vue.use(VueRouter);
const routes = [
    { path: '/bookmark1', component: Bookmark1 },
    { path: '/switch', component: Switch }
  ];

  const router = new VueRouter({
    routes
  });

export default {
  router,
}
</script>

<style>
.app {
    display: flex;
    flex-direction: row;
}

.navigation {
    min-width: 30vw;
    height: 100vh;
    display: flex;
    background: linear-gradient(to bottom, blueviolet, #DCA3E2);
    flex-direction: column;
    align-content: center;
}

.navigation-box {
    padding: 20px;
    border: #64004a solid 2px;
    text-decoration: none;
    color: white;
}

.navigation-box:hover {
    background-color: #64004a;
}

.navigation-box:not(:first-child) {
    border-top: none;
}
</style>
