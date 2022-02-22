<template>
    <main class="debug">
        <section class="main-top">
          <div class="container">
            <h3>Content Goes Here</h3>
          </div>
        </section>
        <section class="main-bottom flex">
          <div class="container flex gallery">
            <div v-for="(item, index) in items" :key="index" class="card flex">
              <img :src="item.icon">
              <span>{{item.text}}</span>
            </div>
          </div>
        </section>
    </main>
</template>

<script>
export default {
  name: 'DcMain',

  data() {

    return {

      items: [

        {
          icon: require("../assets/img/buy-comics-digital-comics.png"),
          text: "Digital Comics"
        },
        {
          icon: require("../assets/img/buy-comics-merchandise.png"),
          text: "DC Merchandise"
        },
        {
          icon: require("../assets/img/buy-comics-subscriptions.png"),
          text: "Subscription"
        },
        {
          icon: require("../assets/img/buy-comics-shop-locator.png"),
          text: "Comic Shop Locator"
        },
        {
          icon: require("../assets/img/buy-dc-power-visa.svg"),
          text: "DC Power Visa"
        }

      ]
    }
  }
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
          width: 40px;
        }
      }
  }
</style>
