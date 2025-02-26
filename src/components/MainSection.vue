<template>
  <div class="container">
    <main class="layout">
      <section class="main-content">
        <div class="image">
          <img src="../assets/image.png" alt="Image with a random draw" />
        </div>
        <div class="text-content">
          <h1 class="title">The Bright Future of Web 3.0?</h1>
          <div class="text-and-button">
            <p class="text">
              We dive into the next evolution of the web that claims to put the
              power of the platforms back into the hands of the people. But is
              it really fulfilling its promise?
            </p>
            <button class="btn">READ MORE</button>
          </div>
        </div>
      </section>
      <aside class="news">
        <h2 class="sub-title">New</h2>
        <div class="news-item">
          <h3 class="news-title">Hydrogen VS Electric Cars</h3>
          <p class="subscription">
            Will hydrogen-fueled cars ever catch up to EVs?
          </p>
        </div>
        <div class="divider"></div>
        <div class="news-item">
          <h3 class="news-title">The Downsides of AI Artistry</h3>
          <p class="subscription">
            What are the possible adverse effects of on-demand AI image
            generation?
          </p>
        </div>
        <div class="divider"></div>
        <div class="news-item">
          <h3 class="news-title">Is VC Funding Drying Up?</h3>
          <p class="subscription">
            Private funding by VC firms is down 50% YOY. We take a look at what
            that means.
          </p>
        </div>
      </aside>
    </main>
  </div>
</template>

<script lang="ts" scoped>
export default {
  name: "App",
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.container {
  font-family: $font-primary;
  margin: 0 auto;
  padding: 20px;
  max-width: 1200px;
}

.layout {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 30px;
}

.main-content {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
}

.image img {
  width: 100%;
}

.text-content {
  margin-top: 10px;
  display: flex;
  gap: 20px;
  align-items: flex-start;
}

.title {
  font-size: 3rem;
  color: $secondary-color;
  font-weight: 800;
  width: 40%;
  margin-right: 15px;
  margin-top: 10px;
}

.text-and-button {
  flex: 1;
}

.text {
  font-size: 1rem;
  color: $gunmetal;
  margin-bottom: 20px;
  margin-left: 25px;
}

.btn {
  background: $vermillion;
  color: $secondary-color;
  padding: 10px 20px;
  margin-left: 25px;
  border: none;
  font-weight: 700;
  cursor: pointer;
  margin-top: 20px;
  letter-spacing: 0.1em;
  &:hover {
    background: $secondary-color;
    color: $primary-color;
  }
}

.news {
  background: $secondary-color;
  padding: 10px;
  height: auto;
}

.sub-title {
  font-size: 2rem;
  color: $yellow;
}

.news-item {
  margin-top: 20px;
}

.news-title {
  font-size: 1.2rem;
  color: $primary-color;
  cursor: pointer;
  &:hover {
    color: $yellow;
  }
}

.subscription {
  font-size: 0.9rem;
  color: $silver;
}

.divider {
  height: 1px;
  background: $silver;
  margin: 20px 0;
}

@media (max-width: 768px) {
  .text-container {
    flex-direction: column;
  }

  .title {
    font-size: 2rem;
  }
  .layout {
    grid-template-columns: 1fr;
  }

  .main-content {
    grid-template-columns: 1fr;
  }

  .news {
    margin-top: 20px;
  }
}
</style>
