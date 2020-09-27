<template>
  <div class="mt-3">
    <label for="input">Search Box</label>
    <input
      type="text"
      v-model="search"
      name="input"
      class="form-control"
      placeholder="You may search the name and press enter ..."
      @change="$emit('filter-result')"
    />
  </div>
</template>
<script>
export default {
  props: ["contents"],
  data() {
    return {
      search: "",
    };
  },
};
</script>

<style scoped>
label {
  color: black;
  font-weight: 500;
}
</style>
