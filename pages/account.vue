<template>
  <v-row justify="center" align="center">
    <v-col>
      <h4>{{ title }}</h4>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Vue } from "nuxt-property-decorator";

@Component
export default class AccountPage extends Vue {
  title = "Account Page";
}
</script>
