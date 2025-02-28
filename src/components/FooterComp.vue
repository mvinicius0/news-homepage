<template>
  <main class="design">
    <section class="footer">
      <div class="footer-content">
        <div class="img">
          <img src="../assets/Bitmap.jpg" alt="old computer" />
        </div>
        <div class="footer-text">
          <h2 class="title-number">01</h2>
          <h3 class="sub_title">Reviving Retro PCs</h3>
          <p class="text-2">
            What happens when old PCs are given modern upgrades?
          </p>
        </div>
      </div>

      <div class="footer-content">
        <span class="img">
          <img src="../assets/keyboard.jpg" alt="old computer" />
        </span>
        <div class="footer-text">
          <h2 class="title-number">02</h2>
          <h3 class="sub_title">Top 10 Laptops of 2022</h3>
          <p class="text-2">Our best picks for various needs and budgets.</p>
        </div>
      </div>

      <div class="footer-content">
        <span class="img">
          <img src="../assets/dualsense.jpg" alt="old computer" />
        </span>
        <div class="footer-text">
          <h2 class="title-number">03</h2>
          <h3 class="sub_title">The Growth of Gaming</h3>
          <p class="text-2">
            How the pandemic has sparked fresh opportunities.
          </p>
        </div>
      </div>
    </section>
  </main>
</template>

<script lang="ts">
export default {
  name: "FooterComp",

  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.design {
  background: $primary-color;
  font-family: $font-primary;
  padding: 20px;
}
.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
  margin-top: 20px;
}

.footer-content {
  display: flex;
  gap: 10px;
}

.img img {
  width: 110px;
  height: 140px;
  margin-top: 30px;
}

.title-number {
  font-size: 32px;
  color: $vermillion;
}

.sub_title {
  font-size: 18px;
  color: $secondary-color;
  font-weight: 800;
  cursor: pointer;

  &:hover {
    color: $vermillion;
  }
}

.text-2 {
  font-size: 13px;
  color: $gunmetal;
}

@media (max-width: 768px) {
  .footer {
    flex-direction: column;
  }

  .img img {
    width: 110px;
    height: 180px;
    margin-top: 30px;
  }

  title-number {
    font-size: 14px;
    color: $vermillion;
  }

  .sub_title {
    font-size: 12px;
    color: $secondary-color;
    font-weight: 800;
    cursor: pointer;
  }

  .text-2 {
    font-size: 12px;
    color: $gunmetal;
  }
}
</style>
