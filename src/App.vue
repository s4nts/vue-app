<template>
  <TheHeader 
    v-show="showHeader"
  />
  <img 
    v-show="1 === 1"
  alt="Vue logo" src="./assets/logo.png" />
  <TheContent />
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
