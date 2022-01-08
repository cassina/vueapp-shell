<template>
  <a :href="link.href"
     class="text-white px-3 py-2 rounded-md text-sm font-medium"
     aria-current="page"> {{ link.name }}
  </a>
</template>

<script lang="ts">
import Vue, {PropOptions} from "vue";
import {INavigationLink} from "~/interfaces/navigation-link.interface";

export default Vue.extend({
  name: "NavigationLink",
  props: {
    link: {
      type: Object,
      required: true,
    } as PropOptions<INavigationLink>
  }
})
</script>