<template>
  <v-app id="inspire">
    <v-container fluid>
      <v-data-iterator
        :items="items"
        :items-per-page.sync="itemsPerPage"
        hide-default-footer
      >
        <template v-slot:default="props">
          <v-row>
            <v-col
              v-for="item in props.items"
              :key="item.name"
              cols="12"
              sm="6"
              md="4"
              lg="3"
            >
              <v-card>
                <v-card-title class="subheading font-weight-bold">{{
                  item.name
                }}</v-card-title>

                <v-divider></v-divider>

                <v-list dense>
                  <v-list-item>
                    <v-list-item-content>Calories:</v-list-item-content>
                    <v-list-item-content class="align-end">{{
                      item.calories
                    }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Fat:</v-list-item-content>
                    <v-list-item-content class="align-end">{{
                      item.fat
                    }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Carbs:</v-list-item-content>
                    <v-list-item-content class="align-end">{{
                      item.carbs
                    }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Protein:</v-list-item-content>
                    <v-list-item-content class="align-end">{{
                      item.protein
                    }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Sodium:</v-list-item-content>
                    <v-list-item-content class="align-end">{{
                      item.sodium
                    }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Calcium:</v-list-item-content>
                    <v-list-item-content class="align-end">{{
                      item.calcium
                    }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Iron:</v-list-item-content>
                    <v-list-item-content class="align-end">{{
                      item.iron
                    }}</v-list-item-content>
                  </v-list-item>
                  <v-list-item>
                    <v-list-item-content>recipe:</v-list-item-content>
                    <v-list-item-content class="align-end">
                      <a href="item.recipe"> Click Here</a>
                    </v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-card>
            </v-col>
          </v-row>
        </template>
      </v-data-iterator>
    </v-container>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    itemsPerPage: 3,
    items: [
      {
        name: "Beef Stuffed Sweet Potato",
        calories: 360,
        fat: 16.0,
        carbs: 34,
        protein: 20.0,
        sodium: 770 + " mg",
        calcium: "NA",
        iron: "NA",
        recipe: null
      },
      {
        name: "Roast Chicken and Veggie",
        calories: 500,
        fat: 22.0,
        carbs: 25,
        protein: 47,
        sodium: 670 + " mg",
        calcium: "NA",
        iron: "NA",
        recipe: null
      },
      {
        name: "Chicken, Pepper and Corn Stir-Fry",
        calories: 420,
        fat: 18.0,
        carbs: 41,
        protein: 22.0,
        sodium: 640 + " mg",
        calcium: "NA",
        iron: "NA",
        recipe:
          "https://www.foodnetwork.com/recipes/food-network-kitchen/chicken-pepper-and-corn-stir-fry-3362501#/"
      }
    ]
  })
};
</script>
