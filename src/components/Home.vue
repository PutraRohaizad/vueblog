<template>
  <div class="container">
    <h2 class="text-center"><u>MyVueBlog</u></h2>

    <!-- Content -->
    <Content :contents="contents" />
  </div>
</template>

<script>
import Content from "./Content";

export default {
  components: {
    Content,
  },
  data() {
    return {
      contents: [],
    };
  },
  created() {
    fetch("https://jsonplaceholder.typicode.com/users")
      .then((res) => res.json())
      .then((data) => (this.contents = data))
      .catch((err) => console.log(err));
  },

};
</script>

<style scoped>

</style>
