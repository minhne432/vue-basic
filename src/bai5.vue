<template>
  <h1>{{ title }} {{ Name }} {{ age }} years old!</h1>
  <button v-on:click="changeTiltle('GoodBye')">click here</button>
  <br />
  <input type="text" @input="changeName($event)" />
  <input type="text" @input="changeAge($event)" />
  <br />
  <input type="text" @keyup.enter="changeName($event)" />
  <input type="text" @keyup.enter="changeAge($event)" />
  <br />
  <form action="" @submit.prevent="formSubmit">
    <input type="text" v-model="Name" />
    <input type="text" v-model="age" />

    <button>Submit</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      title: "Hello",
      Name: "Minh",
      age: 20,
    };
  },
  methods: {
    changeTiltle(my_title) {
      this.title = my_title;
    },
    changeName(event) {
      this.Name = event.target.value;
    },
    changeAge(event) {
      this.age = event.target.value;
    },
    update_inf(my_name, my_Age) {
      this.changeName(my_name);
      this.changeAge(my_Age);
    },
    formSubmit() {
      alert(this.Name);
      alert(this.age);
    },
  },
};
</script>