<template>
    <header>
        <div class="container">
            <nav class="flex">
                <a href="#">
                    <img src="../assets/img/dc-logo.png">
                </a>
                <ul class="flex">
                    <li v-for="(item, index) in links" :key="index">
                        <a :href="item.url">{{item.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
  name: 'DcHeader',

  data() {

      return {

          links: [
              {
                  text: "Characters",
                  url: "#"
              },
              {
                  text: "Comics",
                  url: "#"
              },
              {
                  text: "Movies",
                  url: "#"
              },
              {
                  text: "TV",
                  url: "#"
              },
              {
                  text: "Games",
                  url: "#"
              },
              {
                  text: "Collectibles",
                  url: "#"
              },
              {
                  text: "Videos",
                  url: "#"
              },
              {
                  text: "Fans",
                  url: "#"
              },
              {
                  text: "News",
                  url: "#"
              },
              {
                  text: "Shop",
                  url: "#"
              },
          ]
      }
  }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

    header {
        background-color: white;

        nav {
            justify-content: space-between;
            align-items: center;
            margin-right: 30px;

            ul {
                list-style: none;
                justify-content: space-around;

                li {
                    padding: 35px 15px;
                    text-transform: uppercase;
                    font-weight: bold;
                    border-bottom: 2px solid transparent;

                    &:hover {
                        border-color: $primaryColor;
                    }

                    a {
                        color: $secondaryColor;

                        &:hover {
                            color: $primaryColor;
                        }
                    }

                }
            }

        }
    }
</style>
