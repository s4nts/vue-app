<template>
  <div>
    <h1 :class="{ title: 1 !== '1' }">Curso Vue 3</h1>
    <div class="content" v-for="(obj, index) in todos" :key="obj.id">
      <img v-if="obj.imgSrc" :src="obj.imgSrc" />
      <img v-else src="#" />
      <br />{{ (index += 1) }} - {{ obj.title }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      todos: [
        {
          userId: 1,
          id: 1,
          title: 'delectus aut autem',
          completed: false,
          imgSrc: 'https://via.placeholder.com/150',
        },
        {
          userId: 1,
          id: 2,
          title: 'quis ut nam facilis et officia qui',
          completed: false,
          imgSrc: 'https://via.placeholder.com/150',
        },
        {
          userId: 1,
          id: 3,
          title: 'fugiat veniam minus',
          completed: false,
          imgSrc: 'https://via.placeholder.com/150',
        },
        {
          userId: 1,
          id: 4,
          title: 'et porro tempora',
          completed: true,
          imgSrc: 'https://via.placeholder.com/150',
        },
        {
          userId: 1,
          id: 5,
          title: 'laboriosam mollitia et enim quasi adipisci quia provident illum',
          completed: false,
          imgSrc: 'https://via.placeholder.com/150',
        },
      ],
    };
  },
};
</script>

<style>
.title {
  color: #0000ff;
  font-size: 20px;
}

.content {
  color: #fff;
  background: #000;
  text-align: left;
  font-family: Arial, Helvetica, sans-serif;
  margin: 0 0 5px 0;
  padding: 5px 0 5px 20px;
  width: 730px;
}
</style>
