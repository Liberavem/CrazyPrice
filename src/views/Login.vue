<template>
  <v-app-bar>
    <v-toolbar>
      <v-toolbar-title class="headline text-uppercase">
        <span>Crazy</span>
        <span class="font-weight-light">Price</span>
      </v-toolbar-title>
    </v-toolbar>
  <v-app>
    <v-main>
      <v-container class="mx-auto"
                   >
        <LoginForm/>
      </v-container>
    </v-main>
  </v-app>
    <Footer/>
  </v-app-bar>
</template>
<script>
import LoginForm from "@/components/login/LoginForm";
import Footer from "@/components/common/Footer";

export default {
  components: {Footer, LoginForm}
}
</script>
