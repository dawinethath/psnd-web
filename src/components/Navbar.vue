<template>
<v-card tile>
    <v-app-bar clipped-left app class="primary">
      <v-app-bar-nav-icon class="white--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <SettingPopup />
    </v-app-bar>

    <v-navigation-drawer clipped v-model="drawer" app class="primary">
      <v-list class="mt-12">
        <v-list-item-group color="primary lighten-5">
          <v-list-item v-for="(item, i) in this.items" :key="i">
            <v-list-item-icon>
              <v-icon class="white--text">{{item.icon}}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title class="white--text">{{item.text}}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
</v-card>
</template>

<script>
import SettingPopup from '../components/SettingPopup.vue';
export default {
  props: {
    ninjas: {
      type: String
    }
  },
  data: () => ({
    drawer: false,
    items: [
        {text: 'ស្វែងរកមន្រ្តី', icon: 'mdi-magnify', route: '/'},
        {text: 'គ្រប់​គ្រង​អ្នកប្រើ​ប្រាស់', icon: 'mdi-account-group', route: '/'},
    ]
  }),
  components: {
    SettingPopup
  },
  methods: {
    greet: () => {
      return SettingPopup
    }
  }
}
</script>

<style scoped>
</style>