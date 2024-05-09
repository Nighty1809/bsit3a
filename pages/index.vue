<template>
  <v-card>
    <v-card-title>
      Nutrition
      <v-spacer></v-spacer>
      <v-text-field v-model="search" append-icon="mdi-magnify" label="Search" single-line hide-details></v-text-field>
    </v-card-title>
    <v-data-table :headers="headers" :items="StudentData" :search="search">
      <template slot="item.actions" slot-scope="{item}">
        <v-btn color="#B80000"> DELETE</v-btn>
        <v-btn color="#0079FF"> EDIT</v-btn>
      </template>
    </v-data-table>

  </v-card>
</template>
<script>
export default {
  data() {
    return {
      search: '',
      headers: [
        {
          text: 'ID',
          align: 'start',
          sortable: false,
          value: 'StudentID',
        },
        { text: 'FirtsName', value: 'Firts_Name' },
        { text: 'LastName', value: 'Last_Name' },
        { text: 'MiddleName', value: 'Middle_Name' },
        { text: 'Course', value: 'Course' },
        { text: 'Year', value: 'Year' },
        { text: '', value: "actions" }
      ],
      StudentData: [
        {

          Firts_Name: 'Billy Joe',
          StudentID: '21-00581',
          Last_Name: 'Racines',
          Middle_Name: 'Venus',
          Course: 'BSIT',
          Year: '3rd',
        },
        {

Firts_Name: 'Alyssa',
StudentID: '21-00111',
Last_Name: 'Magday',
Middle_Name: 'Gutierrez',
Course: 'BSIT',
Year: '3rd',
},

      ],
    }
  },
}
</script>