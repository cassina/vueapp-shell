<template>
  <!-- This example requires Tailwind CSS v2.0+ -->
  <nav class="bg-green-900">
    <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
      <div class="relative flex items-center justify-between h-16">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">

          <!-- Mobile hamburger button-->
          <mobile-menu />
          <!-- Mobile hamburger button-->
        </div>

        <div class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start">

          <!-- App Logo-->
          <navigation-logo />

          <!-- Navigation Links-->
          <navigation-links />
        </div>

        <div class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0">

          <!-- Notifications Icon -->
          <navigation-notifications-icon />

          <!-- Profile dropdown -->
          <navigation-user-menu />
        </div>
      </div>
    </div>

    <!-- Mobile menu, show/hide based on menu state. -->
    <navigation-mobile-menu />
  </nav>

</template>

<script>
import MobileMenu from "~/components/MobileMenuButton";
import NavigationLogo from "~/components/NavigationLogo";
import NavigationLinks from "~/components/NavigationLinks";
import NavigationNotificationsIcon from "~/components/NavigationNotificationsIcon";
import NavigationUserMenu from "~/components/NavigationUserMenu";
import NavigationMobileMenu from "~/components/NavigationMobileMenu";
export default {
  name: "Navigation",
  components: {
    NavigationMobileMenu,
    NavigationUserMenu, NavigationNotificationsIcon, NavigationLinks, NavigationLogo, MobileMenu}
}
</script>

<style scoped>

</style>