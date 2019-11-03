<template>
  <v-container>
    <v-data-table :headers="headers" :items="desserts" class="elevation-1">
      <template v-slot:item.calories="{ item }">
        <v-chip :color="getColor(item.calories)" dark>{{
          item.calories
        }}</v-chip>
      </template>
    </v-data-table>
  </v-container>
</template>

<script>
export default {
  name: "fastFood",
  data() {
    return {
      headers: [
        {
          text: "Fast Foods",
          align: "left",
          sortable: false,
          value: "name"
        },
        { text: "Calories", value: "calories" },
        { text: "Fat (g)", value: "fat" },
        { text: "Carbs (g)", value: "carbs" },
        { text: "Protein (g)", value: "protein" },
        { text: "Iron (%)", value: "iron" }
      ],
      desserts: [
        {
          name: "Burger King Whopper (Serving Size 1 whopper (292g))",
          calories: 640,
          fat: 35.0,
          carbs: 52,
          protein: 31.0,
          iron: "70% or 12.7 mg"
        },
        {
          name:
            "Wendy's Old Fashioned Baconator Burger (Serving Size 1 whopper (276g))",
          calories: 830,
          fat: 51.0,
          carbs: 35,
          protein: 56,
          iron: "35%"
        },
        {
          name: "Wendy's Classic-Chocolate-Frosty",
          calories: 350,
          fat: 9.0,
          carbs: 58,
          protein: 10.0,
          iron: "8%"
        },
        {
          name: "Single BONAFIDE Chicken Leg",
          calories: 160,
          fat: 9.0,
          carbs: 5,
          protein: 14,
          iron: "8%"
        },
        {
          name: "Single BONAFIDE Chicken Breast",
          calories: 440,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          iron: "16%"
        },
        {
          name: "McDonald's Big Mac",
          calories: 520,
          fat: 27.0,
          carbs: 45,
          protein: 26.0,
          iron: "25%"
        }
      ]
    };
  },
  methods: {
    getColor(calories) {
      if (calories > 400) return "red";
      else if (calories > 200) return "orange";
      else return "green";
    }
  }
};
</script>
