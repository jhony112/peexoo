<template>
    <div class="container-fluid">
        <div class="row m-0">
            <div class="col-12 col-md-7 col-lg-7 m-0 p-0  d-none d-md-block">
                <div id="carousel" class="carousel slide carousel-fade" data-ride="carousel">
                    <ol class="carousel-indicators">
                        <li data-target="#carousel" data-slide-to="0" class="active"></li>
                        <li data-target="#carousel" data-slide-to="1"></li>
                        <li data-target="#carousel" data-slide-to="2"></li>
                    </ol>
                    <div class="carousel-inner">
                        <div class="carousel-item active">
                            <img class="item-image d-block w-100"
                                 src="https://source.unsplash.com/1000x800/?photography">
                            <div class="caption">
                                <i class="fas fa-map-marker"></i> Benin.Nigeria
                            </div>
                        </div>
                        <div class="carousel-item ">
                            <img class="item-image d-block w-100"
                                 src="https://source.unsplash.com/1000x800/?art,wedding">
                            <div class="caption">
                                <i class="fas fa-map-marker"></i> Lagos Nigeria
                            </div>
                        </div>
                        <div class="carousel-item">
                            <img class="item-image d-block w-100"
                                 src="https://source.unsplash.com/1000x800/?black,youth,happy,american">
                            <div class="caption">
                                <i class="fas fa-map-marker"></i> Irvinton. USA
                            </div>
                        </div>
                    </div>

                </div>
            </div>
            <div class="col-12 col-md-5  info__box">
                <div class="card">
                    <img src="http://beta.peexoo.ai/img/peexoo234.ab7075f3.png" class="	d-block d-sm-none" style="width: 7em;margin-bottom: 10px">
                    <div class="talk__text">
                        <span>Live.</span>
                        <span>Snap.</span>
                        <span>Remember</span>
                    </div>
                    <div class="lora text-left  w-98">
                        Relive your best memories and highlight meaningful moments through the lens of world-class
                        professional photographers around you.
                    </div>
                    <div class="action__area   m-t-50">
                        <div class="row ">
                            <div class="col-12 col-md-6 ">
                                <div class="btn btn-primary btn-block">
                                    <i class="fas fa-search"></i>
                                    <span class="text-bold  m-l-5">Find a photographer</span>
                                </div>
                            </div>
                            <div class="col-12 col-md-6">
                                <div class="btn btn-outline-primary btn-block">
                                    <i class="fas fa-camera"></i>
                                    <span class="text-bold m-l-5">I am a photographer</span>
                                </div>
                            </div>
                        </div>



                    </div>
                    <!--<div class="more">-->
                    <!--<div class="row">-->
                    <!--<div class="col-12 col-md-6">-->
                    <!--<div class="info-box">-->
                    <!--<div class="icon">-->
                    <!--<i class="fas fa-search"></i>-->
                    <!--</div>-->
                    <!--<div class="flex-col">-->
                    <!--<div class="">Peexoo Find</div>-->
                    <!--&lt;!&ndash;<div class="text-muted">&ndash;&gt;-->
                    <!--&lt;!&ndash;Looking to hire a photographer for a personal shoot or to cover an event? We’ve got the best in the business&ndash;&gt;-->
                    <!--&lt;!&ndash;</div>&ndash;&gt;-->
                    <!--</div>-->
                    <!--</div>-->


                    <!--</div>-->
                    <!--<div class="col-12 col-md-6"></div>-->
                    <!--</div>-->
                    <!--</div>-->
                    <div class="reviews m-t-20 text-left">
                        <div class="text-dark"> What some of our users think</div>
                        <div id="carousel2" class="carousel slide review_carousel m-t-20 " data-ride="carousel">

                            <div class="carousel-inner">
                                <div class="carousel-item active review">
                                    <img class="user_image"
                                         src="https://source.unsplash.com/1000x800/?photography">
                                    <div class="info text-left">
                                        <div class="text-bold">Alicia Keys</div>
                                        <star-rating :show-rating="false" :rounded-corners="true" :star-size="10"
                                                     :increment="0.5" :read-only="true" v-model="rating"></star-rating>
                                        <div class="text-italics m-t-5 text-sm">Amazing photo quality i cannot imagine
                                            my wedding pictures any better!!
                                        </div>
                                    </div>
                                </div>


                            </div>

                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="row">
                <div class="col-12 m-t-50">
                    <h2 class="text-bold text-left">Color Scheme Used</h2>
                    <img src="../assets/images/yellow-brown-by-schemecolor.png" style="width: 100%"/>
                </div>

            </div>
        </div>

    </div>
</template>

<script>
    /* eslint-disable no-undef */

    // @ is an alias to /src

    import StarRating from 'vue-star-rating'
    // import Slick from 'vue-slick';

    export default {
        name: 'home',
        components: {
            StarRating
        },
        data() {
            return {
                rating: 5,
            };
        },
        mounted() {
            JQuery('.carousel-fade').carousel({interval: 8000})
            JQuery('.review_carousel').carousel({interval: 6000})
        }
    }
</script>
<style lang="scss">
    .showcase {
        height: 300px;
        width: 300px;

        img {
            width: 100%;
            height: 100%;
        }
    }

    .container-fluid {
        padding-right: 0 !important;
        padding-left: 0 !important;
        background: #f6f6f6 !important;
    }

    .carousel-fade .carousel-item {
        height: 100vh;
        position: relative;
        border-bottom-right-radius: 80px;

        img {
            height: 100%;
            border-radius: inherit;
            width: 100%;
            object-fit: cover;
        }
        .caption {
            position: absolute;
            background: black;
            left: 20px;
            color: white;
            padding: 10px 20px;
            bottom: 50px;
            border-radius: 20px;
        }
    }

    .card {
        border: unset !important;
padding-top: 80px;
        padding-left: 15px;
        padding-right: 15px;

    }



    .talk__text {
        text-align: left;
        width: 80%;
        span {
            font-weight: 800;
            font-size: 2.8em;
            line-height: 1em;
            color: #391D0C;
            letter-spacing: -1px;
            font-family: Raleway, sans-serif;
        }
    }

    .lora {
        font-family: "Proxima Nova", sans-serif !important;
        font-size: 1.7em!important;
        line-height: 1.2em;
        margin-top: 20px;
    }

    .btn {
        padding: 15px 18px !important;
        font-size: 1.1em;
        margin-bottom: 10px;
        /*border-radius: 30px!important;*/
    }

    .review {
        display: flex !important;
        align-items: center;
        width: 80%;
        .user_image {
            width: 4em;
            height: 4em;
            border-radius: 50%;
            object-fit: cover;
        }
        .info {
            margin-left: 5px;
            line-height: .8em;
            width: 70%;
        }

    }
    .info__box {
        position: relative;
    }

    @media screen and (min-width: 750px) {

        .info__box {
            position: absolute;
            top: 80px;
            right: 50px;
            z-index: 100;
        }
        .card {
            border: unset !important;
            min-height: 500px;
            background: #ffffff !important;
            padding: 100px 50px 50px 50px;
            border-top-left-radius: 80px !important;
            border-bottom-right-radius: 80px !important;

        }
        .talk__text {
            text-align: left;
            width: 100%;
            span {

                font-weight: 800;
                font-size: 2.8em;
                color: #391D0C;
                letter-spacing: -1px;
                font-family: Raleway, sans-serif;
            }
        }
    }

    @keyframes Gradient {
        0% {
            background-position: 0% 50%
        }
        50% {
            background-position: 100% 50%
        }
        100% {
            background-position: 0% 50%
        }
    }

    .info-box {
        display: flex;
        align-items: center;

        .icon {
            background: brown;
            color: white;
            border-radius: 5px;
            padding: 10px 15px;

        }
    }

    .btn-primary {
        color: #fff;
        background-color: #863E15 !important;
        border-color: #863E15 !important;
    }

    .btn-outline-primary {
        color: #863E15 !important;
        border-color: #863E15 !important;
    }
</style>
