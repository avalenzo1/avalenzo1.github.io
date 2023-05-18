<template>
  <nav class="navbar gutter" role="navigation" aria-label="Main Navigation" id="navbar">
    <div class="navbar-links">
      <button class="btn" @click="showNav = !showNav"><Icon name="mdi:menu"></Icon></button>
      <transition name="fade">
        <ul class="navbar-nav md:flex-row lg:flex-row" role="Main Navigation" v-if="showNav">
          <li class="nav-item" v-for="link in linkList">
            <NuxtLink class="btn btn-primary" :to="link.to"><Icon :name="link.icon" />{{ link.name }}</NuxtLink>
          </li>
        </ul>
    </transition>
    </div>
    <div class="navbar-logo">
      <a href="/">Ant</a>
    </div>
  </nav>
</template>

<style>
  .fade-enter-active, .fade-leave-active { transition: all .5s; }
  .fade-enter, .fade-leave-active { opacity: 0; transform: translate3d(-100%, -100%, 0) scale(0); }
</style>

<script>
  console.log("%c Ant was here ;)", "background: #000000; color: #F4AA6B");

  // function scrollSpy() {
  //   let navbar = document.getElementById("navbar");

  //   document.addEventListener(
  //     "scroll",
  //     (e) => {
  //       let top = window.pageYOffset || document.documentElement.scrollTop;

  //       if (top > 0) {
  //         navbar.classList.remove("an-navbar--idle");
  //       } else {
  //         navbar.classList.add("an-navbar--idle");
  //       }
  //     },
  //     { passive: true }
  //   );
  // }

  // scrollSpy();

  export default {
    data() {
      return {
        showNav: false,
        linkList: [
          {
            icon: "mdi:home",
            name: "Home",
            to: "/"
          },
          {
            icon: "mdi:information",
            name: "About",
            to: "/about"
          },
          {
            icon: "mdi:projector-screen",
            name: "Projects",
            to: "/projects"
          },
          {
            icon: "mdi:contacts",
            name: "Contacts",
            to: "/contact"
          }
        ]
      }
    }
  }
</script>