<template>
  <header :class="{ 'scrolled-view': scrollPosition }" class="header">
    <div class="branding"><img src="../assets/W..svg" alt="W word" /></div>
    <nav class="nav">
      <ul v-show="!mobile" class="nav-list">
        <li class="item"><router-link to="/">Home</router-link></li>
        <li class="item"><router-link to="/new">New</router-link></li>
        <li class="item"><router-link to="/popular">Popular</router-link></li>
        <li class="item"><router-link to="/trending">Trending</router-link></li>
        <li class="item">
          <router-link to="/categories">Categories</router-link>
        </li>
      </ul>
      <div class="icon">
        <font-awesome-icon
          @click="toggleMobileNav"
          v-show="mobile"
          class="far fa-bars"
          icon="bars"
          :class="{ 'icon-active': mobileNav }"
        />
      </div>
      <transition name="mobile-nav">
        <ul v-show="mobileNav" class="dropdown-nav">
          <li @click="toggleMobileNav" class="item img">
            <img src="../assets/x.svg" alt="" />
          </li>
          <li class="item"><router-link to="/">Home</router-link></li>
          <li class="item"><router-link to="/new">New</router-link></li>
          <li class="item">
            <router-link to="/popular">Popular</router-link>
          </li>
          <li class="item">
            <router-link to="/trending">Trending</router-link>
          </li>
          <li class="item">
            <router-link to="/categories">Categories</router-link>
          </li>
        </ul>
      </transition>
    </nav>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "HeaderComp",

  data() {
    return {
      scrollPosition: false,
      mobile: false,
      mobileNav: false,
      windowWidth: 1700,
    };
  },

  created() {
    window.addEventListener("resize", this.checkScreen);
    this.checkScreen();
  },

  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },

    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 768) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.header {
  background: $primary-color;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-family: $font-primary;
  margin-bottom: 15px;
  padding: 0 20px;
  position: relative;
}

.nav-list {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.branding img {
  width: 69px;
  height: 42px;
}

.item {
  list-style: none;
  margin: 0 15px;
  color: $gunmetal;
  font-size: 0.8rem;
  cursor: pointer;

  &:hover {
    color: $vermillion;
  }
}

.icon {
  display: flex;
  align-items: center;
  position: absolute;
  top: 0;
  right: 24px;
  height: 100%;
  width: 20px;
  cursor: pointer;
  font-size: 24px;
}

.icon-active {
  transform: rotate(180deg);
}

.dropdown-nav {
  display: flex;
  flex-direction: column;
  position: fixed;
  width: 100%;
  max-width: 250px;
  height: 100%;
  background: $primary-color;
  top: 0;
  right: 0;
  margin-top: 0;

  li {
    margin-left: 0;
    margin-top: 10px;
    font-size: 18px;
    color: $secondary-color;
    font-family: $font-primary;
  }

  .img {
    display: flex;
    justify-content: end;
    margin-right: 10px;
    margin-bottom: 80px;
    margin-top: 20px;
  }
}

.mobile-nav-enter-active,
.mobile-nav-leave-active {
  transition: 1s ease all;
}

.mobile-nav-enter-from,
.mobile-nav-leave-to {
  transform: translateX(250px);
}

.mobile-nav-enter-to {
  transform: translateX(0);
}

@media (max-width: 768px) {
  .header {
    flex-direction: column;
    align-items: flex-start;
  }

  .nav-list {
    flex-direction: column;
    align-items: flex-start;
  }

  .item {
    margin: 10px 0;
  }
}
</style>
