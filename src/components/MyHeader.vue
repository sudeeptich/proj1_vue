<template>
  <div>
      <h1>{{ bloodGroupName }}</h1>
    <h2>{{ authorName }}</h2>
  </div>
</template>

<script>
export default {
   name: 'MyHeader',
  props: {
    
    bloodGroupName: String,

        authorName: String
  }
};
</script>

<style scoped>
div {

  text-align: center;
  color: rgb(207, 125, 96); 
  font-size: 1.5em; 
}
</style>