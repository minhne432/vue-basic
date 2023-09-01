

<template>
  <!-- Databinding -->
  <h1>Hello world!</h1>
  <p>name: {{ name }}</p>
  <p v-pre>name: {{ name }}</p>
  <p>age: {{ age }}</p>
  <a :href="link">link: Click to go my website</a>
  <p v-html="content"></p>
  <button :disabled="isDisable">Btn1</button>
  <button :disabled="isDisable1">Btn2</button>
  <img :src="img_link" />
</template>


<script>
export default {
  data() {
    return {
      name: "Nguyễn Hoàng Minh",
      age: 21,
      link: "https://linkneban.fun",
      content: "<strong>Nội dung được in đậm</strong>",
      isDisable: true,
      isDisable1: false,
      img_link:
        "https://areajugones.sport.es/wp-content/uploads/2020/06/one-piece-black-clover.jpg",
    };
  },
};
</script>

