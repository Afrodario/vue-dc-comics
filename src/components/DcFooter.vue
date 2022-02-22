<template>
    <footer>

      <div class="footer-top">
        <div class="container">

          <div class="foot-container flex">
            <div class="footer-list">
                <h3>DC COMICS</h3>
                <ul v-for="(item, index) in comics" :key="index">
                    <li>{{item.text}}</li>
                </ul>
                <h3>SHOP</h3>
                <ul v-for="(item, index) in shop" :key="index">
                    <li>{{item.text}}</li>
                </ul>
            </div>
            <div class="footer-list">
                <h3>DC</h3>
                <ul v-for="(item, index) in dc" :key="index">
                    <li>{{item.text}}</li>
                </ul>
            </div>
            <div class="footer-list">
                <h3>SITES</h3>
                <ul v-for="(item, index) in sites" :key="index">
                    <li>{{item.text}}</li>
                </ul>
            </div>
          </div>
        </div>
      </div>

      <div class="footer-bottom">
        <div class="container flex">
          <button>SIGN-UP NOW!</button>
          <div class="social-panel flex">
            <span>FOLLOW US</span>
            <img src="../assets/img/footer-facebook.png">
            <img src="../assets/img/footer-periscope.png">
            <img src="../assets/img/footer-pinterest.png">
            <img src="../assets/img/footer-twitter.png">
            <img src="../assets/img/footer-youtube.png">
          </div>
        </div>
      </div>
        
    </footer>
</template>

<script>
// import DcFooterList from './components/DcFooterList.vue'

export default {
  name: 'DcFooter',
    data() {

      return {

          comics: [
              {
                  text: "Characters",
              },
              {
                  text: "Comics",
              },
              {
                  text: "Movies",
              },
              {
                  text: "TV",
              },
              {
                  text: "Games",
              },
              {
                  text: "Videos",
              },
              {
                  text: "News",
              }
          ],

          shop: [
              {
                  text: "Shop DC",
              },
              {
                  text: "Shop DC Collectibles",
              }
          ],

          dc: [
              {
                  text: "Terms of Use",
              },
              {
                  text: "Privacy Policy (New)",
              },
              {
                  text: "Ad Choices",
              },
              {
                  text: "Advertising",
              },
              {
                  text: "Jobs",
              },
              {
                  text: "Subscriptions",
              },
              {
                  text: "Talent Workshops",
              },
              {
                  text: "CPSC Certificates",
              },
              {
                  text: "Ratings",
              },
              {
                  text: "Shop Help",
              },
              {
                  text: "Contact Us",
              },                           
          ],

          sites: [
              {
                  text: "DC",
              },
              {
                  text: "MAD Magazine",
              },
              {
                  text: "DC Kids",
              },
              {
                  text: "DC Universe",
              },
              {
                  text: "DC Power Visa",
              },
          ]
      }
  }
  // components: {
  //   DcFooterList,
  // }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

  footer {
    background-color: green;
  }

  .footer-top {
    padding: 20px;
    background-image: url("../assets/img/footer-bg.jpg");

    .foot-container {
        width: 40%;
        justify-content: space-around;
    }

    .footer-list {
      color: $secondaryColor;
      font-size: 15px;
      font-weight: bold;

      ul {
        margin: 10px 0;
      }
    }
  }

  .footer-bottom {
    background-color: #303030;

      button {
        align-self: center;
        color: white;
        background: none;
        padding: 20px;
        font-weight: bold;
        font-size: 15px;
        border: 1px solid $primaryColor;
      }

    .container {
      justify-content: space-between;
      height: 100px;
    }

    .social-panel {
      align-items: center;

      & * {
        padding: 0 10px;
      }

      span {
        color: $primaryColor;
        font-size: 25px;
        text-transform: uppercase;
      }
    }
  }

</style>
