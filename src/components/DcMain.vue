<template>
    <main class="debug">
        <section class="main-top">
          <div class="container">
            <h3>Content Goes Here</h3>
          </div>
        </section>
        <section class="main-bottom flex">
          <div class="container flex gallery">
            <div class="card flex">
              <img src="../assets/img/buy-comics-digital-comics.png">
              <span>Digital Comics</span>
            </div>
            <div class="card flex">
              <img src="../assets/img/buy-comics-merchandise.png">
              <span>DC Merchandise</span>
            </div>
            <div class="card flex">
              <img src="../assets/img/buy-comics-shop-locator.png">
              <span>Subscription</span>
            </div>
            <div class="card flex">
              <img src="../assets/img/buy-comics-subscriptions.png">
              <span>Comic Shop Locator</span>
            </div>
            <div class="card flex">
              <img src="../assets/img/buy-dc-power-visa.svg">
              <span>DC Power Visa</span>
            </div>
          </div>
        </section>
    </main>
</template>

<script>
export default {
  name: 'DcMain',
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";
  main {

      .main-top {
        background-color: #1c1c1c;

        h3 {
          color: white;
          text-align: center;
          font-size: 30px;
        }
      }

      .main-bottom {
        background-color: $primaryColor;
        height: 200px;

        .gallery {
          justify-content: space-between;
        }

        img {
          width: 50px;
        }
      }
  }
</style>
