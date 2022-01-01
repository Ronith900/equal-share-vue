<template>
  <v-container>
    <v-row>
      <v-col v-for="n in 3" :key="n">
        <v-card class="pa-2" outlined tile> One of three columns </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import { Component, Vue } from "nuxt-property-decorator";

@Component
export default class FriendsPage extends Vue {
  title = "Firends Page";
}
</script>
