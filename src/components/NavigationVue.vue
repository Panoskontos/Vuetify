<template>
    <v-table>
    <thead>
      <tr>
        <th class="text-left">
          Name
        </th>
        <th class="text-left">
          Calories
        </th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="item in desserts"
        :key="item.name"
      >
        <td>{{ item.name }}</td>
        <td>{{ item.calories }}</td>
      </tr>
    </tbody>
  </v-table>
</template>


<script>
export default {
    name:'NavigationVue',
    data(){
        return {
            desserts: [
                {
                    name:'Yogurt',
                    calories: 159
                },
                {
                    name:'Yogurt',
                    calories: 159
                },
            ]
        }
    }
}
</script>