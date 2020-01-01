<template>
    <div id="app">
        <header>
            <!-- Fixed navbar -->
            <nav class="navbar navbar-expand-md navbar-dark fixed-top bg-dark navbar-hide">
                <a class="navbar-brand" href="#">
                    <img src="http://beta.peexoo.ai/img/peexoo234.ab7075f3.png" alt="pexoo logo">
                </a>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarCollapse"
                        aria-controls="navbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarCollapse">
                    <ul class="navbar-nav mr-auto">
                        <!--<li class="nav-item active">-->
                        <!--<a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>-->
                        <!--</li>-->
                        <!--<li class="nav-item">-->
                        <!--<a class="nav-link" href="#">Link</a>-->
                        <!--</li>-->
                        <!--<li class="nav-item">-->
                        <!--<a class="nav-link disabled" href="#">Disabled</a>-->
                        <!--</li>-->
                    </ul>

                </div>
            </nav>
        </header>
        <div role="main" >
            <img src="http://beta.peexoo.ai/img/peexoo234.ab7075f3.png" class="h-logo d-none d-md-block">
            <router-view/>
        </div>

    </div>
</template>
<script>
    /* eslint-disable no-undef */


    export default {
        mounted() {
            JQuery(window).scroll(function () {

                // add/remove class to navbar when scrolling to hide/show
                var scroll = $(window).scrollTop();
                if (scroll >= 150) {
                    $('.navbar').removeClass("navbar-hide");
                    $('.h-logo').hide();

                } else {
                    $('.navbar').addClass("navbar-hide");
                    $('.h-logo').show();
                }

            });
        }
    }
</script>
<style scoped>
    @import "assets/fonts/fonts.css";
    @import "assets/css/util.css";
    @import "assets/css/style.css";
    @import "assets/css/slick-theme.css";

    #app {
        font-family: 'proxima_nova', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        width: 100vw;
    }

    main {

    }

    .h-logo {
        width: 8em;
        position: absolute;
        z-index: 10000;
        left: 20px;
        top: 10px;
    }

    #nav {
        padding: 30px;
        z-index: 100;
    }

    #nav a {
        font-weight: bold;
        color: #2c3e50;
    }

    #nav a .router-link-exact-active {
        color: #42b983;
    }




    .footer {
        position: absolute;
        bottom: 0;
        width: 100%;
        /* Set the fixed height of the footer here */
        height: 60px;
        line-height: 60px; /* Vertically center the text there */
        background-color: #f5f5f5;
    }

    /* Custom page CSS
    -------------------------------------------------- */
    /* Not required for template or sticky footer method. */

    body > .container {
        padding: 60px 15px 0;
    }

    .footer > .container {
        padding-right: 15px;
        padding-left: 15px;
    }

    code {
        font-size: 80%;
    }

    .navbar-brand img {

        width: 120px;
    }
    .bg-dark{
       background: #391D0c!important;
    }
</style>
