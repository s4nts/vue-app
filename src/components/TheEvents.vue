<template>
  <div>
    <button v-on:click="onClick">Enviar</button>
  </div>
  <br><br>
  <div @mouseover="onMouseOver" @mouseout="onMouseOut" :v-on="mouseout">
    Mouse over
  </div>
  <br><br>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {};
  },

  methods: {
    onClick($evt) {
      console.log('Executou função click', $evt);
    },
    onMouseOver($evt) {
      console.log('Executou função mouse over', $evt)
    },
    onMouseOut($evt) {
      console.log('Executou função mouse out', $evt);
    }
  },
};
</script>

<style></style>
