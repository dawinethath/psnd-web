<template>
<div>
    <v-btn text icon class="primary white--text" @click="dialog = true">
        <v-icon>mdi-cog-outline</v-icon>
    </v-btn>
    <v-dialog max-width="600px" v-model="dialog">
      <v-card>
        <v-card-title class="headline">Use Google's location service?</v-card-title>

        <v-card-text>
         
        </v-card-text>

        <v-card-actions>
          <v-spacer></v-spacer>

          <v-btn
            color="green darken-1"
            text
            @click="dialog = false"
          >
            Disagree
          </v-btn>

          <v-btn
            color="green darken-1"
            text
            @click="dialog = false"
          >
            Agree
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
</div>
</template>

<script>
export default {
    name: 'SettingPopup',
    data: () => ({
        dialog: false,
    }),
}
</script>