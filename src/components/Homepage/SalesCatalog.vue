<template>
  <v-expansion-panel>
    <v-expansion-panel-content
        v-for="(item,i) in todos"
        :key="i"
    >
      <template v-slot:header>
        <div>{{ item.title}} {{ item.discount}}</div>
      </template>
      <v-card>
        <v-card-text>
          <SalesCard
              v-bind:todo="item"
          />
        </v-card-text>
      </v-card>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
import SalesCard from "@/components/Homepage/SalesCard";

export default {
  props: ['todos'],
  name: "SalesCatalog",
  components: {SalesCard}
}
</script>
