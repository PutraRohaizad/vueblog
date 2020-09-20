<template>
  <div class="jumbotron mt-3">
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
        <tr :key="content.id" v-for="(content, index) in contents">
          <th scope="row">{{index + 1}}</th>
          <td>{{content.name}}</td>
          <td>{{content.username}}</td>
          <td>{{content.email}}</td>
          <td>
            <button class="btn btn-success mr-3">Edit</button>
            <button class="btn btn-danger">Delete</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  props:['contents']
};
</script>

<style>
</style>
