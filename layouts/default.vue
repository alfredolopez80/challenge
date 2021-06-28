<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
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
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-app-bar-title v-text="title" />
      <template v-slot:extension>
        <v-tabs
          class="tabs"
          centered
          grow
          height="60px"
          v-model="model"
        >
          <v-tab v-for="tab in menus" :key="tab.id" :to="tab.to" exact>
            {{ tab.title }}
          </v-tab>
        </v-tabs>

      </template>
    </v-app-bar>

    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear()}} Alfredo Lopez</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    const array = [
      {
        id: 0,
        icon: 'mdi-apps',
        title: 'Welcome',
        to: '/'
      },
      {
        id: 1,
        icon: 'mdi-book-open',
        title: 'RT Orderbook',
        to: '/orderbook'
      },
      {
        id: 2,
        icon: 'mdi-candle',
        title: 'Candlesticks Graphic',
        to: '/candlesgraph'
      },
      {
        id: 3,
        icon: 'mdi-wallet',
        title: 'Wallet Integration',
        to: '/wallet'
      }
    ];
    const menu = array.slice(1,4);
    console.log(menu, array);
    return {
      model:null,
      clipped: false,
      drawer: false,
      fixed: false,
      items: array,
      menus: menu,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Challenge Dapp Vue'
    }
  }
}
</script>
