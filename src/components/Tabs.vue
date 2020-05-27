<template>
<v-container fluid>
  <v-row justify="center">
    <v-col
    cols="12"
    sm="12"
    md="10"
    >
      <v-tabs background-color="primary" grow show-arrows v-model="tab" > 
          <v-tab v-for="(tab,t) in tabs" :key="t">
            <v-icon left> {{tab.icon}} </v-icon>
            <span> {{tab.text}} </span>
          </v-tab>
      </v-tabs>
        <v-tabs-items v-model="tab">
          <v-tab-item>
            <!-- Leave it empty -->
          </v-tab-item>
          <v-tab-item class="mt-5 pt-5">
            <v-row no-gutters justify="space-around">
              <v-col 
              cols="12"
              sm="12"
              md="2"
              >
                <v-text-field
                flat
                solo
                readonly
                :label="labels[0]"
                ></v-text-field>
              </v-col>
              <v-col
              cols="12"
              sm="11"
              md="6"
              >
                <v-select
                dense
                deletable-chips
                chips
                rounded
                :items="seleteItems" 
                filled 
                :label="labels[1]"></v-select>
              </v-col>
              <v-col
              cols="12"
              sm="11"
              md="3"
              >
                <v-select
                dense
                deletable-chips
                chips
                rounded
                :items="seleteItems" 
                filled 
                :label="labels[2]"></v-select>
              </v-col>
            </v-row>
            <v-divider></v-divider>
          </v-tab-item>
        </v-tabs-items>
    </v-col>
  </v-row>
</v-container>
</template>

<script>
export default {
  name: 'Tabs',
  data: () => ({
    labels: ['អង្គ.ថ្នាក់ស្មើអគ្គ','អង្គស្នងការដ្ទាននគរបានជាតិ', 'អង្គស្នងការដ្ទាននគរបានជាតិ'],
    tab: '',
    tabs: [
      {text: 'ស្វែងរក', icon: 'mdi-magnify'},
      {text: 'អង្គភាព', icon: 'mdi-account-box-multiple'}
    ],
    seleteItems: ['Foo', 'Bar', 'Fizz', 'Buzz'],
  }),
}
</script>

<style scoped>
</style>