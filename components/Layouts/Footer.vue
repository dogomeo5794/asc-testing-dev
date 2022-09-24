<template>
  <v-footer :absolute="!fixed" app>
    <!-- <span>&copy; {{ new Date().getFullYear() }}</span> -->
    <div class="footer-nav">
      <ul>
        <li>Terms and Conditions</li>
        <li>Privacy Policy</li>
        <li>Inquiry</li>
      </ul>
    </div>
    <div class="footer-details">
      <span>
        Ad Standards Council - Screening System -v 2.0
        <br />
        &copy; 2022. Ad Standards Council
      </span>
    </div>
  </v-footer>
</template>

<style scoped>
  ul, li{
    vertical-align: middle;
    display: flex;
    text-decoration: underline;
    padding: 0em 1em;
  }

  li:hover{
      cursor: pointer;
  }
  .footer-nav{
      float: left;
  }
  .footer-details{
      float: right;
  }
</style>
