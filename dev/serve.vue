<script>
import Vue from 'vue';
import Vue2NetworkStatus from '@/vue2-network-status.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    Vue2NetworkStatus
  }
});
</script>

<template>
  <div id="app">
    <vue2-network-status />
  </div>
</template>
