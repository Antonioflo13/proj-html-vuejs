<template>
    <!-- main -->
    <main>

        <!-- foodie journal -->
        <section class="journal-container">
            <h3>foodie Journal</h3>

            <div class="article-container">

                <article class="article-box">
                    <img src="../assets/images/single-post-img3-400x263.jpg" alt="">
                    <h3>Food Corner: Top Japanese Restaurant for sushi</h3>
                    <h6>By Admin I 25th, 2019</h6>
                </article>

                <article class="article-box">
                    <img src="../assets/images/fi-roundup-400x263.jpg" alt="">
                    <h3>Food Corner: Top Japanese Restaurant for sushi</h3>
                    <h6>By Admin I 25th, 2019</h6>
                </article>

                <article class="article-box">
                    <img src="../assets/images/fi-toasts-400x263.jpg" alt="">
                    <h3>Food Corner: Top Japanese Restaurant for sushi</h3>
                    <h6>By Admin I 25th, 2019</h6>
                </article>

            </div>

        </section>
        <!-- /foodie journal -->

    </main>
    <!--/ main -->
</template>

<script>
export default {
    name:"main",
}
</script>

<style lang="scss" scoped>
    @import "../style/mixin.scss";
    @import "../style/variables.scss";
    main {
        font-family: "vidaloka", sans-serif;
    }
    .journal-container {
        @include wrapper;
        position: absolute;
        top: 700px;
        left: 50%;
        right: 50%;
        transform: translate(-50%);
        padding: 20px;
        background-color: white;
        margin: 1% auto;

        h3:first-child {
            font-family: "catamaran", sans-serif;
            font-size: 21px;
            font-weight: bold;
            text-transform: uppercase;
            text-align: center;
        }

        h3 {
            cursor: pointer;
            transition: 1s;
        }
        h3:hover {
            text-decoration: underline;
            color: $third-txt-color;
        }

        .article-container {
            display: flex;
        }

        .article-box {
            img {
                width: 350px;
                margin-bottom: 20px;
            }
            margin: 1%;
            text-align: center;
            h6 {
                font-family: "catamaran", sans-serif;
                color: $second-txt-color;
            }
        }
    }
</style>