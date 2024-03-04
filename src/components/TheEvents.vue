<template>
  <div>
    <button v-on:click="onClick()">Enviar</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {};
  },

  methods: {
    onClick() {
      console.log('Executou função click');
    },
  },
};
</script>

<style></style>
