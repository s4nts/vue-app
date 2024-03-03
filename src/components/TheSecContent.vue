<template>
  <div>
    One-way data binding <br />
    Two-way data binding <br />
    v-model => formulários
  </div>
  <br /><br />
  <label>Nome</label><br />
  <input v-model="name" type="text" />
  <br />
  {{ name }}
  <br /><br />
  <div>
    <select v-model="sports">
      <option value="">Escolha</option>
      <option value="basquete">Basquete</option>
      <option value="futebol">Futebol</option>
      <option value="volei">Vôlei</option>
    </select>
    <br /><br />
    {{ sports }}

    <br /><br />

    <input v-model="newslatter" type="radio" value="Sim" />Sim
    <input v-model="newslatter" type="radio" value="Não" />Não
    <br />
    {{ newslatter }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      sports: '',
      newslatter: 'Sim',
    };
  },
};
</script>

<style></style>
