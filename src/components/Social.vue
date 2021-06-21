<template>
    <!-- Social -->
    <ul>

        <li>
            <a href=""><i class="fab fa-facebook-f"></i></a>
        </li>
        <li>
            <a href=""><i class="fab fa-instagram"></i></a>
        </li>
        <li>
            <a href=""><i class="fab fa-twitter"></i></a>
        </li>
        <li>
            <a href=""><i class="fab fa-youtube"></i></a>
        </li>
        <li>
            <a href=""><i class="fab fa-tiktok"></i></a>
        </li>
        <li>
            <a href=""><i class="fab fa-pinterest-p"></i></a>
        </li>

     </ul>
    <!-- /Social -->
</template>

<script>
export default {
    name: "Social"
}
</script>

<style lang="scss" scoped>
    @import "../style/variables.scss";
    @import "../style/mixin.scss";
    ul li {
        @include list-inline;
        a {
            font-size: 17px;
            text-decoration: none;
            padding: 0 15px;
            color: #3f3c39;
            :hover {
                color: #837E77;
            }
        }
    }
</style>