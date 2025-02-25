<template>
  <section class="main-section">
    <span class="image">
      <img src="../assets/image.png" alt="Image with a random draw" />
    </span>

    <h1 class="title">The Bright Future of Web 3.0?</h1>
    <div class="content">
      <p class="text">
        We dive into the next evolution of the web that claims to put the power
        of the platforms back into the hands of the people. But is it really
        fulfilling its promise?
      </p>
      <button class="btn">READ MORE</button>
    </div>

    <div class="news">
      <h2 class="sub-title">New</h2>
      <div class="group-1">
        <h3 class="news-title">Hydrogen VS Electric Cars</h3>
        <p class="subscription">
          Will hydrogen-fueled cars ever catch up to EVs?
        </p>
      </div>
      <div class="divider">
        <img src="../assets/divider.svg" alt="A divider" />
      </div>
      <div class="group-2">
        <h3 class="news-title">The Downsides of AI Artistry</h3>
        <p class="subscription">
          What are the possible adverse effects of on-demand AI image
          generation?
        </p>
      </div>
      <div class="divider">
        <img src="../assets/divider.svg" alt="A divider" />
      </div>
      <div class="group-3">
        <h3 class="news-title">Is VC Funding Drying Up?</h3>
        <p class="subscription">
          Private funding by VC firms is down 50% YOY. We take a look at what
          that means.
        </p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: "MainSection",

  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.main-section {
  font-family: $font-primary;
  margin-left: 10px;
}

.image img {
  width: 38rem;
}

.title {
  font-size: 56px;
  color: $secondary-color;
  font-weight: 800;
  width: 20rem;
  margin-top: 15px;
}

.content {
  width: 15rem;
  position: relative;
  left: 22rem;
  bottom: 15rem;
}

.content p {
  font-size: 14px;
  color: $gunmetal;
}

.content button {
  color: $secondary-color;
  background: $vermillion;
  font-size: 14px;
  border: none;
  width: 185px;
  height: 48px;
  font-weight: 700;
  cursor: pointer;
  letter-spacing: 0.25em;
  margin-top: 30px;

  &:hover {
    background: $secondary-color;
    color: $primary-color;
  }
}

.news {
  background: $secondary-color;
  width: 20rem;
  position: relative;
  left: 40rem;
  bottom: 44.6rem;
  height: 500px;
}

.news h2 {
  font-size: 40px;
  color: $yellow;
  margin: 20px;
  padding-top: 10px;
}

.news-title {
  font-size: 20px;
  color: $primary-color;
  cursor: pointer;
  margin: 20px;

  &:hover {
    color: $yellow;
  }
}

.subscription {
  font-size: 15px;
  color: $silver;
  margin: 20px;
}
</style>
