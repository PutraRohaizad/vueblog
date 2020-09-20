<template>
  <div class="container">
    <!-- Search filter -->
      <Search></Search>
    <!-- Content -->
      <Content :contents="contents"></Content>
    <!-- Controller Crud -->
    <Controller></Controller>
  </div>
</template>

<script>
import Search from './Search'
import Content from './Content'
import Controller from './Controller'

export default {
  components:{
    Search, Content, Controller
  },
  data(){
    return {
      contents:[]
      
    }
  },
  created(){
    fetch('https://jsonplaceholder.typicode.com/users')
    .then(res => res.json())
    .then(data => this.contents = data)
    .catch(err => console.log(err))
  }

}
</script>

<style>

</style>