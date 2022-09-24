<template>
  <v-app color="red" dark>
    <v-app-bar
      color="white"
      fixed
      app
      height="86"
      light
    >
      <img
        style="max-height: 60px;max-width: 136px;"
        src="/logo/asc-logo.jpg"
      />

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
    <v-main color="red" class="main-wrapper">
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer
      app
      light
      style="justify-content: space-between;padding: 10px 0;"
    >
      <div class="footer-nav">
        <ul class="navbar-nav-footer mr-auto">
          <li class="nav-item active">
            <a href="#" class="nav-link">
              Terms and Conditions
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">
              Privacy Policy
            </a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">
              Inquiry
            </a>
          </li>
        </ul>
      </div>
      <div class="footer-details">
        <span>
          Ad Standards Council - Screening System -v 2.0
          <br />
          &copy; {{ new Date().getFullYear() }}.
          Ad Standards Council
        </span>
      </div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "landing-layout",
  data: () => ({

  })
}
</script>

<style scoped>
  .main-wrapper {
    background: url(/logo/login-bg.png) no-repeat center center fixed;
    background-size: cover;
  }
  .navbar-nav {

  }
  .navbar-nav .nav-item,
  .footer-nav .navbar-nav-footer .nav-item {
    list-style: none;
    display: inline;
  }
  /* .navbar-nav .nav-item:first-child {
    margin-left: auto;
  }
  .navbar-nav .nav-item:last-child {
    margin-right: auto;
  } */
  .navbar-nav .nav-link,
  .footer-nav .navbar-nav-footer .nav-link {
    padding: 0.5rem;
    text-decoration: none;
    color: black;
    font-size: 0.9rem;
  }

  .footer-nav .navbar-nav-footer .nav-link {
    text-decoration: underline;
    font-weight: 500;
  }
  .footer-details span {
    line-height: 1.4rem;
    font-size: 0.9rem;
    font-weight: 500;
  }
</style>
