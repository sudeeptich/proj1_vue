<template>
  <div>
      <SingleBlood v-for="bloodGroup in bloodGroups" :key="bloodGroup._id" :bloodGroup="bloodGroup" />
  </div>
</template>

<script>
 import SingleBlood from '@/components/SingleBlood.vue';

export default {
    name: 'BloodBox',
   props: {
     bloodGroups: Array
  },
   components: {
    SingleBlood
  }
};
</script>

<style>

</style>