<template>
  <!-- START HEADER -->
  <header>
    <div class="bar">
      <div class="navbar">
        <div ref="logo" v-on:click="logo()" class="logo link d-f-c m-c">
          <img src="~assets/img/first-logo.png">
        </div>
        <div class="resp-nav" ref="respNav" v-on:click="navbar">
          <i class="fas fa-bars" aria-hidden="true"></i>
          <i class="fas fa-times d-n" aria-hidden="true"></i>
        </div>
        <div class="nav-navbar d-f-c m-c to-space-between" ref="navnavbar">
          <nav>
            <ul class="ul-navbar">
              <li class="li-navbar">
                <NuxtLink to="/" class="a-navbar showFooter">Home</NuxtLink>
              </li>

              <li class="li-navbar">
                <NuxtLink to="/aboutme" class="a-navbar hideFooter">About me
                </NuxtLink>
              </li>

              <li class="li-navbar">
                <NuxtLink to="/myservices" class="a-navbar hideFooter">
                  My Services
                </NuxtLink>
              </li>

              <li class="li-navbar">
                <a class="a-navbar" href="https://frs99.github.io/portfolio-old/">My portfolio</a>
              </li>
            </ul>
          </nav>
          <nav>
            <NuxtLink to="/contact" class="btn-a">contact</NuxtLink>
          </nav>
        </div>
      </div>
    </div>
  </header>
</template>

<script>

export default {
  name:'Navbar',
  methods: {
    //FOR ADD LINK TO LOGO
    logo: function(){
      window.location.href = "/";
    },
    //FOR NAVBAR WITH RESPONSIVE
    navbar: function(){
      //nav list
      let listNav = this.$refs.navnavbar;
      //icons
      let respNav = this.$refs.respNav;
      listNav.classList.toggle("nav-open");
      respNav.children[0].classList.toggle("d-n");
      respNav.children[1].classList.toggle("d-n");
    },
  },
}
</script>