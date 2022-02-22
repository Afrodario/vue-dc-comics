<template>
    <main class="debug">
        <section class="main-top">
          <div class="jumbotron">
          </div>
          <div class="container flex">
            <h2 class="label">CURRENT SERIES</h2>
            <DcComicCard
              v-for="(comic, index) in comics"
              :key="index"
              :thumb="comic.thumb"
              :series="comic.series"
            />
            <button class="more-comics">LOAD MORE</button>
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
import DcComicCard from "../components/DcComicCard.vue";

export default {
  name: 'DcMain',
  components: {
    DcComicCard,
  },

  data() {

    return {
      // Inizio array items
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

      ],
      // Fine array items

      // Inizio array comics
      comics: [
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
            price: "$19.99",
            series: "Action Comics",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
            price: "$3.99",
            series: "American Vampire 1976",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
            price: "$16.99",
            series: "Aquaman",
            type: "graphic novel"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
            price: "$2.99",
            series: "Batgirl",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
            price: "$3.99",
            series: "Batman",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
            price: "$2.99",
            series: "Batman Beyond",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
            price: "$3.99",
            series: "Batman/Superman",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
            price: "$4.99",
            series: "Batman/Superman Annual",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
            price: "$5.99",
            series: "Batman: The Joker War Zone",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
            price: "$6.99",
            series: "Batman: Three Jokers",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
            price: "$4.99",
            series: "Batman: White Knight Presents: Harley Quinn",
            type: "comic book"
          },
          {
            thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
            price: "$16.99",
            series: "Catwoman",
            type: "graphic novel"
          }
        ]
        // Fine array comics
    }
  }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";
  main {

      .main-top {
        background-color: #1c1c1c;
        padding-bottom: 30px;

        .jumbotron {
          height: 400px;
          background-image: url("../assets/img/jumbotron.jpg");
        }

        .container {
          justify-content: space-around;
          flex-wrap: wrap;
          width: calc(100% / 2 - 10px);
          padding: 60px 0;
          position: relative;
        }
      }

      .label {
            position: absolute;
            top: -20px;
            left: -20px;
            color: white;
            border: 1px solid $primaryColor;
            padding: 10px;
            background-color: $primaryColor;
          }

      .more-comics {
          position: absolute;
          bottom: -10px;
          background-color: $primaryColor;
          border-color: $primaryColor;
          color: white;
          padding: 6px;
          width: 180px;
          font-weight: bold;
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
