<template>
    <header>
        <div class="container">
            <nav class="flex">
                <a href="#">
                    <img src="../assets/img/dc-logo.png">
                </a>
                <ul class="flex">
                    <li>Test</li>
                    <li>Test</li>
                    <li>Test</li>
                    <li>Test</li>
                    <li>Test</li>
                    <li>Test</li>
                    <li>Test</li>
                    <li>Test</li>
                    <li>Test</li>
                    <li>Test</li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
  name: 'DcHeader',
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
                    padding: 15px;
                    color: $secondaryColor;
                    text-transform: uppercase;
                    font-weight: bold;

                    &:hover {
                        color: $primaryColor;
                    }
                }
            }

        }
    }
</style>
