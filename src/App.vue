<template>
  <TheHeader v-if="showHeader" />
  <div class="logg-status" v-if="acessLevel === 1">Olá, {{ user1 }}!</div>
  <div class="logg-status" v-else-if="acessLevel === 2">Olá, {{ user2 }}!</div>
  <div class="logg-status" v-else-if="acessLevel === 3">Olá, {{ user3 }}!</div>
  <div class="logg-status" v-else>{{ undefined }}</div>

  <img v-if="showImg" alt="Vue logo" src="./assets/logo.png" />
  <TheContent v-if="showContent" />
  <TheSecContent />
  <div class="logg-user" v-if="showName">Name: {{ firstName }} {{ LastName }}</div>
  <TheFooter v-if="showFooter" />
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheContent from './components/TheContent.vue';
import TheSecContent from './components/TheSecContent.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheContent,
    TheSecContent,
    TheFooter,
  },
  data() {
    return {
      showHeader: false,
      showContent: false,
      acessLevel: 3,
      user1: 'Usuário Admin',
      user2: 'Usuário Marketing',
      user3: 'Usuário',

      showImg: 1 !== 1,
      showName: false,
      firstName: 'Wyulle',
      LastName: 'Santos',
      showFooter: false,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0 0 20px 200px;
}

.logg-status {
  text-align: start;
  color: #fff;
  background: #2c3e50;
  margin: 95px 0 20px 0;
  padding: 20px 0 20px 10px;
  border-radius: 5px;
  width: 250px;
}

.logg-user {
  text-align: start;
  color: #fff;
  background: #2c3e50;
  margin: 20px 0 20px 0;
  padding: 20px 0 20px 10px;
  border-radius: 5px;
  width: 250px;
}
</style>
