<template>
  <div class="jumbotron mt-3">
    <!-- Search filter -->
    <div class="m-3">
      <label for="input">Search Box</label>
      <input
        type="text"
        v-model="search"
        name="input"
        class="form-control"
        placeholder="You may search the name and press enter ..."
      />
    </div>

    <table class="table table-hover">
      <thead>
        <tr class="text-white bg-dark">
          <th scope="col">#</th>
          <th scope="col">Name</th>
          <th scope="col">Username</th>
          <th scope="col">Email</th>
          <th scope="col">Action</th>
        </tr>
      </thead>
      <tbody>
        <tr :key="content.id" v-for="(content, index) in filters">
          <th scope="row">{{ index + 1 }}</th>
          <td>{{ content.name }}</td>
          <td>{{ content.username }}</td>
          <td>{{ content.email }}</td>
          <td>
            <!-- Controller Crud -->
            <Controller></Controller>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import Controller from "./Controller";

export default {
  props: ["contents"],
  data(){
    return {
      search:''
    }
  },
  components: {
    Controller,
  },
  computed: {
    filters:function() {
      return this.contents.filter((content) => {
        return content.name.match(this.search);
      });
    },
  },
};
</script>

<style scoped>
label {
  color: black;
  font-weight: 500;
}
</style>
