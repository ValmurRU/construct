<template>
  <div id="app">
    <ConstructOrder/>
  </div>
</template>

<script>
import { mapActions } from 'vuex';
import ConstructOrder from './components/ConstructOrder.vue';

export default {
  components: {
    ConstructOrder,
  },
  created() {
    window.addEventListener('resize', this.updateClientDeviceWidth);
  },
  methods: {
    ...mapActions([
      'updateClientDeviceWidth',
    ]),
  },
};
</script>

<style>
</style>
