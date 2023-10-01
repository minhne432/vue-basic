<template>
  <!--phần DOM -->
  <h1 v-if="check">{{ title }}</h1>
  <h2>{{ count }}</h2>
  <button @click="increament">+1</button>
  <button @click="($event) => (check = !check)">Show/Hide</button>

  <input type="text" v-model="title" />

  <br />
  <ul>
    <li :key="i" v-for="(animals, i) in animals">{{ animals }}</li>
  </ul>
</template>


<script>
// phần model
export default {
  data() {
    return {
      title: "hello ban hien",
      title2: "hello ban hien 2",
      count: 0,
      animals: ["fish", "cat", "dog"],
      check: true,
    };
  },
  methods: {
    increament() {
      this.count++;
    },
  },
};
</script>
