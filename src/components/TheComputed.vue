<template>
  <div>
    <h1>{{ fullName }}</h1>
    <button>Click Here</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      user: {
        first_name: 'Jon',
        last_name: 'Snow',
      },
    };
  },
  computed: {
    fullName() {
      return `${this.user.first_name} ${this.user.last_name}`;
    },
  },
  methods: {},
};
</script>

<style>
.App {
  color: #000;
}
</style>
