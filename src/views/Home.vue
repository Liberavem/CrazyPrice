<template>
  <div>
    <SearchForm/>
    <SalesCatalog
      v-bind:todos="todos"/>
    <Footer/>
  </div>
</template>
<script>

import SalesCatalog from "@/components/Homepage/SalesCatalog";
import Footer from "@/components/common/Footer";
import SearchForm from "@/components/common/SearchForm";

export default {
  name: 'list',
  data() {
    return{
      todos: [
        {id: 1, title: "Milano Cafe Minsk", img:"https://cdn.vuetifyjs.com/images/cards/cooking.png", work: "10.00-22.00", discount: "-20%", rating: "4.5"},
        {id: 2, title: "Pizzeria IL Grottino", img:"https://cdn.vuetifyjs.com/images/cards/cooking.png", work: "09.00-18.00", discount: "-15%", rating: "4.9"},
        {id: 3, title: "AIR-SHOP.BY",img:"https://cdn.vuetifyjs.com/images/cards/cooking.png", work: "11.00-23.00", discount: "-30%", rating: "4.5"},
        {id: 4, title: "Milano Cafe Minsk", img:"https://cdn.vuetifyjs.com/images/cards/cooking.png", work: "07.00-23.00", discount: "-25%", rating: "4.6"},
        {id: 5, title: "TokiNY", img:"https://cdn.vuetifyjs.com/images/cards/cooking.png", work: "10.00-23.00", discount: "-10%", rating: "4.3"},
        {id: 6, title: "Sherlock Coffee Hall", img:"https://cdn.vuetifyjs.com/images/cards/cooking.png", work: "08.00-22.00", discount: "-10%", rating: "4.2"},
      ]
    }

  },
  components: {SearchForm, Footer, SalesCatalog}
}
</script>
