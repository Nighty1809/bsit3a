<template>
    <v-data-table
      :headers="headers"
      :items="desserts"
      :items-per-page="5"
      class="elevation-1"
    ></v-data-table>
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

      desserts:[
        
      ]
    }
  },
}
</script>