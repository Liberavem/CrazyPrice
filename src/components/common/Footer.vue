<template>
  <v-footer
      fixed="true"
      color="#40bfef"
      height="60"
  >
    <v-row
        justify="center"
        no-gutters
    >
      <v-col
          class="text-center white--text"
      >
        {{ new Date().getFullYear() }} — <strong>EXADEL</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
name: "Footer"
}
</script>

<style scoped>

</style>
