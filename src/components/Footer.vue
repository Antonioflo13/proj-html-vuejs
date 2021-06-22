<template>
  <footer>

      <!-- subscribe -->
      <section>
          <article id="subscribe">
              <h2>Subscribe <span>&</span> Receive A Free eBook</h2>
              <h4>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quo, consequuntur ipsum. A, voluptatem error quisquam provident temporibus labore est autem?</h4>
              <input type="search" placeholder="Insert your email...*">
              <button>subscribe</button>
              
          </article>
      </section>
    <!-- /subscribe -->

  </footer>
</template>

<script>
export default {
    name: "Footer"

}
</script>

<style lang="scss" scoped>
    @import "../style/variables.scss";
    footer {
        height: 300px;
        margin-top: 100px;
        background-image: url(../assets/images/subscribe-sec-bg.png);
        background-position: bottom;
        background-size: cover;
    }
    #subscribe {
        display: flex;
        flex-direction: column;
        align-items: center;
        h2 {
            font-family: "vidaloka", sans-serif;;
            font-size: 35px;
            span {
                color: $third-txt-color;
            }
        }
    }
</style>