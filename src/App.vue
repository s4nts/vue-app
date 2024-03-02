<template>
  <TheHeader v-if="showHeader" />
  <div v-if="acessLevel === 1">Olá, {{ user1 }}!</div>
  <div v-else-if="acessLevel === 2">Olá, {{ user2 }}!</div>
  <div v-else-if="acessLevel === 3">Olá, {{ user3 }}!</div>
  <div v-else>{{ undefined }}</div>

  <img v-if="showImg" alt="Vue logo" src="./assets/logo.png" />
  <TheContent />
  <div v-if="showName">
    firstName: {{ firstName }} <br />
    LastName: {{ LastName }}
  </div>
  <TheFooter />
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheContent from './components/TheContent.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheContent,
    TheFooter,
  },
  data() {
    return {
      showHeader: true,
      acessLevel: 1,
      user1: 'Usuário Admin',
      user2: 'Usuário Marketing',
      user3: 'Usuário',

      showImg: 1 === 1,
      showName: 1 !== '1',
      firstName: 'Jon',
      LastName: 'Snow',
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
