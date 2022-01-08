<template>
  <div class="hidden sm:block sm:ml-6">
    <div class="flex space-x-4">
      <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
      <navigation-link v-for="link in links"
                       :key="link.name"
                       :link="link"/>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import {INavigationLink} from "~/interfaces/navigation-link.interface";
import NavigationLink from "~/components/NavigationLink.vue";
export default Vue.extend({
  name: "NavigationLinks",
  components: {NavigationLink},
  data() {
    return {
      navigationLinks: [
        {
          href: '#',
          name: 'Dashboard'
        },
        {
          href: '#',
          name: 'Basic'
        },
        {
          href: '#',
          name: 'Lifestyle'
        },
        {
          href: '#',
          name: 'Savings'
        },
        {
          href: '#',
          name: 'Income'
        },
      ]
    }
  },
  computed: {
    links(): INavigationLink[] {
      return this.navigationLinks;
    }
  }
});
</script>