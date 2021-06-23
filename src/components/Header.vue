<template>

    <!-- header -->
    <header>
        <section>
            
            <!-- Header-top -->
            <article>

                <!-- Download App -->
                <ul>
                    <li>
                        <a href=""><h5>Download App <span>iOS</span></h5></a>
                    </li>
                    <li>
                        <a href=""><h5>Advertise with us</h5></a>
                    </li>
                </ul>
                <img src="../assets/images/avada-food-logo.png" alt="">
                <Social class="social"/>
                <!-- /Dowmload App -->

                
            </article>
            <!-- /Header-top -->

            <!-- nav-bar -->
            <nav>
                <ul>
                    <li v-for="(links, index) in links" :key="index">
                        <a class="nav-bar-link" href="">{{links}}</a>
                    </li>
                    <li>
                        <a href=""><i class="fas fa-search"></i></a>
                    </li>
                </ul>
            </nav>
            <!-- /nav-bar -->

            <!-- jumbotron -->
            <div class="jumbotron">

                <!-- food-corner -->
                <section>
                    <article>
                        <div>
                            <h6>TODAY'S PICKS</h6>
                        </div>
                        <a href="#"><h1>Food Corner: Top Japanese Retraurants for sushi</h1></a>
                        <h4>March 25, 2019</h4>
                    </article>
                </section>
                <!-- /food-corner -->

            </div>
            <!-- /jumbotron -->
            
        </section>
    </header>
    <!-- /header -->

</template>

<script>
import Social from '../components/Social'

export default {

    components: {
    Social,
  },
  props: ["links"],
}
</script>

<style lang="scss" scoped>
    @import "../style/mixin.scss";
    @import "../style/variables.scss";

    // header
    header {
        position: relative;
        section {
            padding: 10px 0 0 0;
            article {
                @include wrapper;
                display: flex;
                justify-content: space-between;
                align-items: flex-start;
                ul {
                    padding: 0;
                    li {
                        @include list-inline;
                        padding: 5px 0 0 0;
                        a {
                            text-decoration: none;
                            color: rgb(31, 31, 31);
                            :hover {
                            transition: 0.5s;
                            color: $third-txt-color;
                            }
                            h5 {
                            padding: 0 15px 0 0;
                            font-size: 14px;
                            }
                            span {
                            padding: 1px 5px;
                            border-radius: 2px;
                            font-size: 10px;
                            color: white;
                            background-color: $third-txt-color;
                            }
                        }
                    }
                }
                .social {
                    padding: 5px 0 0 0;
                }
            }
            // nav
            nav {
                @include wrapper;
                text-align: center;
                ul li {
                    padding: 0 22px;
                    @include list-inline;
                    a {
                        font-size: 18px;
                        font-weight: bold;
                        text-decoration: none;
                        padding: 0 0 10px 0;
                        color: black;
                        &:hover {
                            color: $third-txt-color;
                        }
                        &:focus {
                            border-bottom: 2px solid $third-txt-color; 
                        }
                        &::after  {
                            display:block;
                            content: '';
                            border-bottom: 2px solid $third-txt-color;  
                            transform: scaleX(0);  
                            transition: transform 250ms ease-in-out;
                        }
                        &:hover:after {
                            transform: scaleX(1);
                        }
                    }
                }
            }
            // jumbotron
            .jumbotron {
                display: flex;
                justify-content: center;
                align-content: center;
                background-image: url(../assets/images/single-post-img3-1200x790.jpg);
                background-position: center;
                background-size: cover;
                font-family:"vidaloka", sans-serif;
                section {
                    display: flex;
                    justify-content: center;
                    align-content: center;
                    padding: 180px 0;
                    article {
                        width: 65%;
                        display: flex;
                        flex-direction: column;
                        align-items: center;
                        padding: 50px 50px;
                        border-radius: 20px;
                        text-align: center;
                        background-color: white;
                        h4 {
                            color: $second-txt-color;
                        }
                        div {
                            position: relative;
                            width: 30%;
                            h6 {
                                position: absolute;
                                bottom: 26px;
                                padding: 10px 30px;
                                border-radius: 10px;
                                color: white;
                                background-color: $third-txt-color;
                            }
                        }
                    }
                }
            }
        }
    }

</style>