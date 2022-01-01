<template>
  <v-row>
    <h4>{{ title }}</h4>
  </v-row>
</template>

<script lang="ts">
import { Component, Vue } from "nuxt-property-decorator";

@Component
export default class FriendsPage extends Vue {
  title = "Firends Page";
}
</script>
