<template>
  <navigation />
</template>

<script lang="ts">
import Vue from 'vue'
import Navigation from "~/components/Navigation.vue";

export default Vue.extend({
  name: 'IndexPage',
  components: {Navigation},
})
</script>
