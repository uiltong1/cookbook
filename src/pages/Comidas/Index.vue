<template>
  <q-page>
    <div class="row" style="border-bottom: solid 1px #26A69A; margin: 0px 20px 0px 20px; margin-bottom: 10px;">
      <h5 style="margin: 10px 0px 10px 30px; color:#26A69A;">Comidas</h5>
    </div>
    <div class="row reverse" style="margin-right:20px;">
      <q-btn color="secondary" label="Novo"/>
    </div>
    <!-- Tabela para listagem de dados -->
    <div>
      <div class="q-pa-md">
        <q-table
          :data="data"
          :columns="columns"
          row-key="name"
        />
      </div>
    </div>
  </q-page>
</template>
<script>
export default {
  data () {
    return {
      columns: [
        {
          name: 'name',
          required: true,
          label: 'Nome do Prato',
          align: 'left',
          field: row => row.name,
          format: val => `${val}`,
          sortable: true,
          classes: 'bg-grey-2 ellipsis',
          headerClasses: 'bg-secondary text-white'
        },
        { name: 'calories', align: 'center', label: 'Nome', classes: 'bg-grey-2 ellipsis', headerClasses: 'bg-secondary text-white', field: 'calories', sortable: true },
        { name: 'fat', label: 'Porção', classes: 'bg-grey-2 ellipsis', headerClasses: 'bg-secondary text-white', field: 'fat', sortable: true },
        { name: 'carbs', label: 'Tempo médio', classes: 'bg-grey-2 ellipsis', headerClasses: 'bg-secondary text-white', field: 'carbs' },
        { name: 'protein', label: 'Preço médio', classes: 'bg-grey-2 ellipsis', headerClasses: 'bg-secondary text-white', field: 'protein' },
        { name: 'sodium', label: 'Ação', classes: 'bg-grey-2 ellipsis', headerClasses: 'bg-secondary text-white', field: 'sodium' }
        // { name: 'calcium', label: 'Calcium (%)', field: 'calcium', sortable: true, sort: (a, b) => parseInt(a, 10) - parseInt(b, 10) },
        // { name: 'iron', label: 'Iron (%)', field: 'iron', sortable: true, sort: (a, b) => parseInt(a, 10) - parseInt(b, 10) }
      ],
      data: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          sodium: 87,
          calcium: '14%',
          iron: '1%'
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          sodium: 129,
          calcium: '8%',
          iron: '1%'
        },
        {
          name: 'Eclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          sodium: 337,
          calcium: '6%',
          iron: '7%'
        },
        {
          name: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          sodium: 413,
          calcium: '3%',
          iron: '8%'
        },
        {
          name: 'Gingerbread',
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          sodium: 327,
          calcium: '7%',
          iron: '16%'
        },
        {
          name: 'Jelly bean',
          calories: 375,
          fat: 0.0,
          carbs: 94,
          protein: 0.0,
          sodium: 50,
          calcium: '0%',
          iron: '0%'
        },
        {
          name: 'Lollipop',
          calories: 392,
          fat: 0.2,
          carbs: 98,
          protein: 0,
          sodium: 38,
          calcium: '0%',
          iron: '2%'
        },
        {
          name: 'Honeycomb',
          calories: 408,
          fat: 3.2,
          carbs: 87,
          protein: 6.5,
          sodium: 562,
          calcium: '0%',
          iron: '45%'
        },
        {
          name: 'Donut',
          calories: 452,
          fat: 25.0,
          carbs: 51,
          protein: 4.9,
          sodium: 326,
          calcium: '2%',
          iron: '22%'
        },
        {
          name: 'KitKat',
          calories: 518,
          fat: 26.0,
          carbs: 65,
          protein: 7,
          sodium: 54,
          calcium: '12%',
          iron: '6%'
        }
      ]
    }
  }
}
</script>
