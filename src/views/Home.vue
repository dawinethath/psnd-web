<template>
<v-container fluid class="grey lighten-5">
  <Tabs></Tabs>
  <SearchTable></SearchTable>
</v-container>
</template>

<script>
import Tabs from '@/../src/components/Tabs.vue';
import SearchTable from '@/../src/components/SearchTable.vue';



export default {
  name: 'Home',
  data: () => ({

  }),
  components: {
    Tabs,
    SearchTable
  },
  methods: {
    
  }
}
</script>