<template>
  <v-card>
  <v-system-bar
    color="blue-grey"
  />
    <v-list>
      <v-list-item>
        <v-spacer></v-spacer>
        <v-list-item-avatar>
          <v-img src="https://cdn.vuetifyjs.com/images/john.png"></v-img>
        </v-list-item-avatar>
        <v-spacer></v-spacer>
      </v-list-item>
      <v-list-item link>
        <v-list-item-content>
          <v-list-item-title class="title">kimhg</v-list-item-title>
          <v-list-item-subtitle>kimhg951117@gmail.com</v-list-item-subtitle>
        </v-list-item-content>
        <v-list-item-action>
          <v-icon>mdi-menu-down</v-icon>
        </v-list-item-action>
      </v-list-item>
    </v-list>

    <v-divider />
    
    <v-list
      nav
      dense
    >
      <v-list-item-group v-model="item" color="primary">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    item: 0,
    items: [
      { text: 'Keywords', icon: 'mdi-folder' },
      { text: 'Chart', icon: 'mdi-account-multiple' },
      { text: '', icon: 'mdi-star' },
    ],
  }),
}
</script>

<style>

</style>