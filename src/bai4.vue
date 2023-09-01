<template>
  <h1>Function (Methods)</h1>
  <h3>{{ hello() }}</h3>
  <h3>{{ hello_1("Ly Thi Cam Ly") }}</h3>
  <h3>{{ hello_2() }}</h3>
  <h3>{{ count }}</h3>
  <button @click="increase">+1</button>
  <button :disabled="isDisable" @click="decrease">-1</button>
</template>


<script>
export default {
  data() {
    return {
      full_name: "Nguyen Hoang Minh",
      count: 0,
      isDisable: false,
    };
  },
  methods: {
    hello() {
      return "Hello " + this.full_name;
    },
    hello_1(my_name) {
      return "Hello " + my_name;
    },
    hello_2: () => {
      //chú ý khi sử dụng .this keyword trong arrow function
      // return "hello" + this.full_name; ---> throw an ERROR
      return "arrow function";
    },
    increase() {
      if (this.count <= 0) {
        this.isDisable = true;
        this.count++;
      } else {
        this.isDisable = false;
        this.count++;
      }
    },
    decrease() {
      this.isDisable = this.count <= 0 ? true : false;
      if (this.count <= 0) {
        this.isDisable = true;
      } else {
        this.isDisable = false;
        this.count--;
      }
    },
  },
};
</script>
