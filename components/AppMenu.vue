<template>
  <div id="navbar" class>
    <div class="top1-menu">
      <a href="index.html">
        <div id="logo" class="ml-2 ml-md-4">
          <img src="~assets/images/download__2_-removebg-preview.png" alt />
        </div>
      </a>

      <div class="top-menu d-none d-lg-block">
        <nuxt-link exact to="/" class="navlink">Home</nuxt-link>
        <nuxt-link exact to="/" class="navlink">About</nuxt-link>
        <nuxt-link exact to="/" class="navlink">Services</nuxt-link>
        <nuxt-link exact to="/" class="navlink">Blog</nuxt-link>
        <nuxt-link exact to="/" class="navlink">Contact</nuxt-link>
      </div>
    </div>
    <label for="toggle">
      <div class="bt">
        <img src="~assets/images/bars-solid.svg" class="hamburger d-lg-none p-1" alt for="toggle" />
      </div>
    </label>
    <input id="toggle" class="d-none" type="checkbox" />
    <a href="#" target class="d-none">Call us:+2348163752417</a>
    <div class="sidebar">
      <div id="menu" class="d-flex">
        <nuxt-link exact to="/">Home</nuxt-link>
        <nuxt-link exact to="/">About</nuxt-link>
        <nuxt-link exact to="/">Services</nuxt-link>
        <nuxt-link exact to="/">Blog</nuxt-link>
        <nuxt-link exact to="/">Contact</nuxt-link>
      </div>
      <img class="bub" src="~/assets/images/bubble.png" />
      <img class="bub1" src="~/assets/images/bubble.png" />
      <img class="bub2" src="~/assets/images/bubble.png" />
      <img class="bub3" src="~/assets/images/bubble.png" />
      <img class="bub4" src="~/assets/images/bubble.png" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuitems: ["Home", "About", "Services", "Blog", "Contact"],
    };
  },
};
</script>

<style >
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.hamburger {
  position: fixed;
  right: 30px;
  top: 20px;
  height: 37px;
  width: 35px;
  z-index: 2010000;
  font-size: 25px;
  font-weight: bolder;
  background-color: rgba(16, 50, 73, 0.678);
  box-shadow: 6px 6px 14px 0 rgba(21, 77, 182, 0.5) inset,
    -8px -8px 18px 0 rgba(10, 68, 156, 0.74) inset;
  cursor: pointer;
  border-radius: 15%;
  line-height: 70px;
}

.hamburger i {
  justify-content: center;
  align-items: inherit;
  z-index: 300000;
}
.hamburger:hover {
  border-radius: 25%;
  background-color: rgba(6, 112, 199, 0.678);
}
#logo {
  line-height: 45px;
  width: 110px;
  z-index: 300;
}

#logo img {
  width: 100%;
}

.top-menu {
  display: inline-block;
  line-height: 45px;
  text-align: center;
  top: 0;
  width: 70vw;
  margin-left: 15vw;
}

.top-menu a {
  margin: 0 15px;
  text-decoration: none;
  color: rgba(0, 76, 95, 0.8);
  font-size: 20px;
}
.navlink {
  position: relative;
}
.navlink::before {
  content: "";
  position: absolute;
  left: 0;
  bottom: -2px;
  background-color: rgba(4, 40, 65, 0.678);
  width: 100%;
  height: 2px;
  transform: scaleX(0);
  transform-origin: center;
  transition: transform 650ms;
}
.navlink:hover::before {
  transform: scaleX(1);
}
#menu {
  flex-direction: column;
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  width: 240px;
  z-index: 50000;
}
#menu a {
  color: white;
  font-size: 23px;
  line-height: 38px;
  text-decoration: none;
  padding: 2px 0;
  cursor: pointer;
}

.sidebar {
  position: fixed;
  top: 40px;
  height: 20vh;
  right: -300px;
  margin-top: 0;
  top: -300px;
  transition: 0.75s ease-out;
  border-radius: 49% 50% 50% 49% / 49% 51% 49% 51%;
  color: whitesmoke;
  z-index: 200;
}

.sidebar::before {
  content: "";
  position: absolute;
  background-image: url("~assets/images/bub.jpg");
  background-size: cover;
  background-position: left;
  height: 100%;
  width: 100%;
  opacity: 0.9;
  border-radius: 68% 0% 0% 83% / 53% 0% 0% 46%;
  z-index: -1;
  box-shadow: 6px 6px 14px 0 rgba(8, 112, 182, 0.959) inset,
    -8px -8px 18px 0 rgb(2, 34, 82) inset;
  transition: 0.75s ease-in;
}

.sidebar a:hover {
  font-size: 25px !important;
  color: rgba(4, 40, 65, 0.9) !important;
}

#toggle:checked ~ .sidebar {
  right: 0px;
  top: 2px;
  border-radius: 68% 0% 0% 83% / 53% 0% 0% 46%;
  height: 70vh;
  transition: 0.75s ease-out;
}

.bub {
  position: absolute !important;
  height: 30px;
  right: 0;
  z-index: -1;
}

.bub1 {
  position: absolute !important;
  height: 40px;
  right: 60px;
  top: 40px;
  z-index: -1;
  transition: 0.9s ease-in-out;
}

.bub2 {
  position: absolute !important;
  height: 50px;
  right: 140px;
  top: 390px;
  z-index: -1;
}

.bub3 {
  position: absolute !important;
  height: 70px;
  right: 160px;
  top: 210px;
  z-index: -1;
}

.bub4 {
  position: absolute !important;
  height: 40px;
  right: 110px;
  top: 290px;
  z-index: -1;
}

@media (min-width: 276px) {
  #logo {
    position: absolute;
    top: 7px;
  }
  #navbar {
    height: 0;
  }
}

@media (min-width: 992px) {
  .top1-menu {
    background: #eaeef6;
    position: fixed;
    width: 100vw;
    z-index: 4400;
    height: 45px;
  }

  #logo {
    position: fixed;
  }
}
</style>