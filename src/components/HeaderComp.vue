<template>
  <header class="header">
    <div class="title"><img src="../assets/W..svg" alt="W word" /></div>
    <nav class="nav-header">
      <ul class="nav-list">
        <li class="item"><router-link to="/">Home</router-link></li>
        <li class="item"><router-link to="/new">New</router-link></li>
        <li class="item"><router-link to="/popular">Popular</router-link></li>
        <li class="item"><router-link to="/trending">Trending</router-link></li>
        <li class="item">
          <router-link to="/categories">Categories</router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
export default {
  name: "HeaderComp",

  data() {
    return {};
  },
};
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
}

.nav-list {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.title img {
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
