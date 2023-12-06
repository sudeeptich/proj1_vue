<template>
    <div :class="{ 'blood-group-container': true, 'green': bloodGroup.willing === 'yes', 'red': bloodGroup.willing === 'no' }">
        <h2>Blood Group: {{ bloodGroup.blood_group }}</h2>
       <h2>Donor: {{ bloodGroup.donor }}</h2>

    <h2>Recipient: {{ bloodGroup.recipient }}</h2>
       <h2>Nature: {{ bloodGroup.nature }}</h2>
         <h2>Willing: {{ bloodGroup.willing }}</h2>
  </div>
</template>


<script>
    export default {
  name: 'SingleBlood',
  props: {

    bloodGroup: Object
  }
};
</script>



<style scoped>

.blood-group-container {
    
  background-color: rgb(228, 90, 90);
  color: rgb(46, 22, 22);
  
  padding: 1em;
  text-align: center;
  margin: 1em;
  border: 2px solid rgb(162, 177, 224);

  border-radius: 8px;
}
</style>