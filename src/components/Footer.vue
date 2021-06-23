<template>
  <footer>

      <!-- subscribe -->
      <section id="bg" >
            <article id="subscribe">
                <h2>Subscribe <span>&</span> Receive A Free eBook</h2>
                <h4 class="mb-5">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quo, consequuntur ipsum. A, voluptatem error quisquam provident temporibus labore est autem?</h4>
                <div id="input" class="mb-5">
                    <input type="search" placeholder="Insert your email...*">
                    <button>subscribe</button>
                </div>
                <h4>Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, doloremque?</h4>
          </article>
      </section>
    <!-- /subscribe -->

    <!-- image -->
    <section id="image">
        <img src="../assets/images/Yogurt-Nan-400x263.jpg" alt="">
        <img src="../assets/images/Mixed-fruits-400x263.jpg" alt="">
        <img src="../assets/images/r-rachel-park-366508-unsplash-min-400x263.jpg" alt="">
        <img src="../assets/images/r-michelle-tsang-500721-unsplash-min-400x263.jpg" alt="">
    </section>
    <!-- /image -->

    <!-- bottom-footer -->
    <section id="bottom-footer">

        <!-- social -->
        <article id="social" class="item">
            <img class="mb-5" src="../assets/images/avada-food-logo-mob-2x-200x87.png" alt="">
            <Social id="social-icon"/>
        </article>
        <!-- /social -->
        <!-- social -->
        <article id="links" class="item">
            <ul>
                <li v-for="(links, index) in links" :key="index">
                    <a class="nav-bar-link" href="">{{links}}</a>
                </li>
            </ul>
        </article>
        <!-- /social -->
        <!-- social -->
        <article id="contacts" class="item">
            <h3 class="mb-3">contact</h3>
            <h4>755 New York Ave, Brooklyn, New York 12203</h4>
            <a href="#"><h4>+0100-505-0000</h4></a>
            <a href="#"><h4>info@you-domain.com</h4></a>
        </article>
        <!-- /social -->
        <!-- social -->
        <article id="get-app" class="item">
            <h3 class="mb-3">get our app!</h3>
            <img class="mb-3" src="../assets/images/download-android-200x66.png" alt="">
            <img src="../assets/images/download-app-store-200x66.png" alt="">
        </article>
        <!-- /social -->

    </section>
    <!-- /bottom-footer -->

  </footer>
</template>

<script>
import Social from '../components/Social'

export default {
    name: "Footer",
    components: {
        Social,
    },
    props: ["links"]

}
</script>

<style lang="scss" scoped>
    @import "../style/variables.scss";
    @import "../style/mixin.scss";
    #bg {
        margin-top: 100px;
        background-image: url(../assets/images/subscribe-sec-bg.png);
        background-position: 64% 68%;
        background-repeat: no-repeat;
        background-size: 136%;
    }
    #subscribe {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 60px;
        h2 {
            font-family: "vidaloka", sans-serif;;
            font-size: 35px;
            span {
                color: $third-txt-color;
            }
        }
        #input {
            width: 100%;
            display: flex;
            justify-content: center;
            input {
                width: 60%;
                padding: 10px;
                border: 1px solid #b4b4b4;
                margin-right: 2%;
            }
            button {
                padding: 10px 40px;
            }
        }
    }
    #image {
        img {
            width: calc(25%);
        }
    }
    #bottom-footer {
        display: flex;
        padding: 50px;
        .item {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: calc(25%);
            padding: 20px;
            border-right: 1px dotted #b4b4b4;
            h3 {
                text-align: left;
                font-size: 16px;
                color: $third-txt-color;
            }
            h4 {
                text-align: center;
            }
        }
        .item:last-of-type {
            border: none;
        }
        #social {
            align-items: center;
            #social-icon {
                padding: 0;
            }
            img {
                max-width: 60%;
            }
        }
        #links {
            li:first-of-type {
                display: none;
            }
            ul {
                padding-left: 0;
            }
            ul li {
                list-style: none;
                padding: 10px;
                a {
                    padding: 10px 10px;
                    font-size: 18px;
                    text-decoration: none;
                    color: #333338;
                    &:hover {
                        color: $third-txt-color;
                    }
                }
            }
        }
        #contacts {
            a {
                h4 {
                    &:hover {
                        color: $third-txt-color;
                    }
                }
            }
        }
        #get-app {
            img {
                max-width: 60%;;
            }
        }
        
    }
    
    // media-query
    @media screen and (min-width: 424px) and (max-width: 768px ) {
        #bottom-footer {
            .item {
                h3 {
                    line-height: 15px;
                    font-size: 12px;
                }
            }
            #links {
                ul li a {
                    font-size: 12px;
                }
            }
        }
        #contacts {
            h4 {
                line-height: 15px;
                font-size: 12px;
            }
        }
    }

</style>