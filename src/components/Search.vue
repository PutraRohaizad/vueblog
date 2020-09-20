<template>
  <div class="mt-3">
    <div>
        <label for="input">Name</label>
      <input type="text" name="name" class="form-control" placeholder="name ">
    </div>
     <div>
        <label for="username">Username</label>
      <input type="text" name="username" class="form-control" placeholder="username ">
    </div>
     <div>
        <label for="email">Email</label>
      <input type="text" name="email" class="form-control" placeholder="email ">
    </div>
    <div class="m-2 text-center">
      <button class="btn btn-primary">Add</button>
    </div>
  </div>
</template>
<script>
export default {

}
</script>

<style scoped>

label{
  color: black;
  font-weight: 500;
}

div > label{
  margin: 10px;
}

</style>