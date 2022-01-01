<template>
  <v-navigation-drawer
    v-model="drawer"
    :miniVariant="miniVariant"
    :clipped="clipped"
    fixed
    app
  >
    <v-list>
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :to="item.to"
        router
        exact
      >
        <v-list-item-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title v-text="item.title" />
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "nuxt-property-decorator";

@Component
export default class ESDrawer extends Vue {
  @Prop({ type: Boolean }) drawer!: Boolean;
  @Prop({ type: Boolean }) clipped!: Boolean;
  @Prop({ type: Boolean }) fixed!: Boolean;
  @Prop({ type: Boolean }) miniVariant!: Boolean;

  private items: Array<object> = [
    {
      icon: "mdi-apps",
      title: "Home",
      to: "/",
    },
    {
      icon: "mdi-chart-bubble",
      title: "Groups",
      to: "/groups",
    },
    {
      icon: "mdi-chart-bubble",
      title: "Friends",
      to: "/friends",
    },
    {
      icon: "mdi-chart-bubble",
      title: "Activity",
      to: "/activities",
    },
    {
      icon: "mdi-chart-bubble",
      title: "Account",
      to: "/account",
    },
  ];
}
</script>
