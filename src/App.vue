<template>

  <div>

    <MyHeader bloodGroupName="Blood Group" authorName="Sudeepti" />

        <BloodBox :bloodGroups="bloodGroups" />
  </div>
</template>

<script>
import MyHeader from '@/components/MyHeader.vue';

import BloodBox from '@/components/BloodBox.vue';

export default {
  name: 'App',
  components: {
    MyHeader,
    BloodBox
  },
  data() {
    return {
      bloodGroups: []
    };
  },
  methods: {
    async fetchBloodGroups() {
      try {
        const res = await fetch('http://localhost:8746/api');
        if (!res.ok) {
          throw new Error(`blood groups ERROR: ${res.statusText}`);
        }
        const data = await res.json();
        return data;
      } catch (error) {
        console.error('ERROR in blood groups:', error);
        return [];
      }
    }
  },
  async created() {
    this.bloodGroups = await this.fetchBloodGroups();
  }
};
</script>

<style>

</style>