<template>
<v-container fluid>
    <v-row justify="center">
        <v-col
        cols="12"
        sm="12"
        md="10"
        >
            <v-card>
                <v-card-title>
                    <v-text-field
                        v-model="search"
                        append-icon="mdi-magnify"
                        :label="labels[0]"
                        single-line
                        hide-details
                        clearable
                    ></v-text-field>
                </v-card-title>
                <v-data-table
                    :headers="headers"
                    :items="datasets"
                    :search="search"
                    @click:row="handleClick"
                ></v-data-table>
            </v-card>
        </v-col>
    </v-row>
</v-container>
</template>

<script>
const axios = require('axios').default;
export default {
    name: 'SearchTable',
    data: () => ({
        labels: ['ស្វែងរក'],
        search: '',
        headers: [
            {
                text: 'gID',
                align: 'start',
                filterable: true,
                value: 'gID',
                divider: false,
                class: "primary white--text"
            },
            { 
                text: 'gName',
                value: 'gName',
                class: "primary white--text" 
            },
        ],
        datasets: [],
    }),
    methods:{
        handleClick(value) {
            // Put your code here
            value.name
        },
    },
    mounted: async function(){
        try {
            const response = await axios.get('http://localhost:3000/dev/general_comm');
            this.datasets = response.data;
        } catch (error) {
            console.error(error);
        }
    }
}
</script>

<style>

</style>