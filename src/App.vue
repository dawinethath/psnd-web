<template>
  <v-app style="font-family: 'Battambang' 28px;">
    <!-- Top -->
    <Navbar></Navbar>
    <v-content>
      <router-view></router-view>
    </v-content>
    <!-- bottom -->
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
export default {
  name: 'App',
  components: {
    Navbar,
  },

  data: () => ({
    //
  }),
};
</script>
