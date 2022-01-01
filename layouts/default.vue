<template>
  <v-app dark>
    <ESDrawer />
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-{{ `chevron-${miniVariant ? "right" : "left"}` }}</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script lang="ts">
import { Component, Vue } from "nuxt-property-decorator";
import ESDrawer from "@/components/drawer.vue";
@Component({
  components: {
    ESDrawer,
  },
})
export default class DefaultLayout extends Vue {
  title: string = "Equal Share";
  clipped: any = true;
  drawer: any = false;
  fixed: any = false;
  miniVariant: any = false;
}
</script>
