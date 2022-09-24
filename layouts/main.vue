<template>
  <v-app dark>
    <v-navigation-drawer
      :mini-variant="miniVariant"
      clipped
      fixed
      app
    >
      <v-app-bar-nav-icon
        @click.stop="miniVariant = !miniVariant"
      />
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
      color="white"
      clipped-left
      fixed
      app
      height="86"
      light
    >
      <v-img
        max-height="60"
        max-width="136"
        src="https://asconlineapp.com/assets/images/asc-logo.jpg"
      ></v-img>

      <ul class="navbar-nav mr-auto">
        <li class="nav-item active">
          <a href="#" class="nav-link">Home </a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Features</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Pricing</a>
        </li>
      </ul>

    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer
    :clipped="clipped"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
