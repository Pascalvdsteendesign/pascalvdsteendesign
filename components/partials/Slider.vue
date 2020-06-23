<template>
<section class="container projects">
    <div class="my-slider">
        <VueSlickCarousel v-bind="settings">
            <a href="#" class="thumb">
                <div class="bg-image" :style="{ 'background-image': 'url(' + 'https://images.unsplash.com/photo-1587613989342-7e21016caff3?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=934&q=80' + ')' }"> </div>
                <div class="thumb-inner">
                    <div class="h5">development</div>
                    <h1 class="h3 border-b">Mondani</br> Farm</h1>
                    <div class="h5">Meer informatie</div>
                </div>

            </a>
            <a href="#" class="thumb">
                <div class="bg-image" :style="{ 'background-image': 'url(' + 'https://images.unsplash.com/photo-1517174637803-6929e01b6e63?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=934&q=80' + ')' }"> </div>
                <div class="thumb-inner">
                    <div class="h5">development & design</div>
                    <h1 class="h3 border-b">Thanda </br>ECB</h1>
                    <div class="h5">Meer informatie</div>
                </div>
            </a>
            <a href="#" class="thumb">
                <div class="bg-image" :style="{ 'background-image': 'url(' + 'https://images.unsplash.com/photo-1587613989342-7e21016caff3?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=934&q=80' + ')' }"> </div>
                <div class="thumb-inner">
                    <div class="h5">development</div>
                    <h1 class="h3 border-b">Byldis</br><span>In opdracht van Nexwork</span></h1>
                    <div href="#" class="h5">Meer informatie</div>
                </div>
            </a>
            <a href="#" class="thumb">
                <div class="bg-image" :style="{ 'background-image': 'url(' + 'https://images.unsplash.com/photo-1517174637803-6929e01b6e63?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=934&q=80' + ')' }"> </div>
                <div class="thumb-inner">
                    <div class="h5">development & design</div>
                    <h1 class="h3 border-b">Hoeve</br> doodleger</h1>
                    <div class="h5">Meer informatie</div>
                </div>
            </a>
            <a href="#" class="thumb">
                <div class="bg-image" :style="{ 'background-image': 'url(' + 'https://images.unsplash.com/photo-1587613989342-7e21016caff3?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=934&q=80' + ')' }"> </div>
                <div class="thumb-inner">
                    <div class="h5">Contact</div>
                    <h1 class="h3 border-b">Uw project</br> hier?</h1>
                    <div class="h5">Meer informatie</div>
                </div>
            </a>

        </VueSlickCarousel>
        <div class="blur">
        </div>
    </div>
</section>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
    data() {
        return {
            settings: {
                "infinite": true,
                pauseOnHover: true,
                "slidesToShow": 4,
                "swipeToSlide": true,
                "arrows": true,
                "autoplay": true,

                "initialSlide": 2,
                "responsive": [{
                        "breakpoint": 1024,
                        "settings": {
                            "slidesToShow": 3,
                        }
                    },
                    {
                        "breakpoint": 767,
                        "settings": {
                            "slidesToShow": 2,

                        }
                    },

                ]
            },
        }
    },

    components: {
        VueSlickCarousel
    },
}
</script>

<style lang="scss">
.projects {
    position: relative;
    height: 500px;
    overflow: hidden;

    @include respond-to(xl) {
        margin-top: -1rem;
    }

    .my-slider.slick-active {
        opacity: 1;
    }

    .slick-current {
        .bg-image {
            opacity: 1 !important;
        }

        .thumb-inner,
        .h5,
        .h3,
        a {
            color: $color-secondary;
        }

        .border-b {
            border-bottom: solid 5px $color-secondary;
        }
    }

    .slick-next {
        right: 12rem;
        top: 11rem;
        z-index: 9;

        &:before {
            font-size: 50px;
            color: $color-primary;
        }

        @include respond-to (md) {
            right: 7rem;
        }

        @include respond-to (lg) {
            right: 10rem;
        }

        @include respond-to (xl) {
            right: 12rem;
        }
    }

    .my-slider {
        position: relative;

        .blur {
            position: absolute;
            right: -0.5rem;
            top: 0;
            background: $color-secondary;
            width: calc(100% / 2);
            height: 110%;
            display: block;
            opacity: 0.96;
            filter: blur(12px);
            -webkit-filter: blur(8px);

            @include respond-to (md) {
                width: calc(100% / 3);
            }

            @include respond-to (xl) {
                width: calc(100% / 4);
            }
        }

        .thumb {
            position: relative;
            height: 480px;
            width: 100%;

            .bg-image {
                position: absolute;
                height: 100%;
                width: 100%;
                background-size: cover;
                opacity: 0;
                transition: ease 300ms;

                &:after {
                    content: '';
                    position: absolute;
                    width: 100%;
                    height: 100%;
                    top: 0;
                    left: 0;
                    background: rgba(0, 0, 0, 0.5);
                    opacity: 1;
                    transition: all 0.5s;
                    -webkit-transition: all 0.5s;
                    -moz-transition: all 0.5s;
                }

            }

            .thumb-inner {
                position: absolute;
                z-index: 999;
                padding: 8rem 2rem 2rem 2rem;
                opacity: 1;
                transition: ease 300ms;

                span {
                    font-size: 16px;
                }

                .h5 {
                    line-height: 1.2;
                }

                a {
                    text-decoration: none;
                }
            }

            &:hover {
                color: $color-secondary;

                .bg-image {
                    opacity: 1;
                }

                .h5,
                .h3,
                    {
                    color: $color-secondary !important;
                }

                a {
                    color: $color-secondary !important;
                }

                .border-b {
                    border-bottom: solid 5px $color-secondary;
                }
            }

            &:hover~.slick-current .bg-image {
                opacity: 0 !important;
            }

        }

    }

}
</style>
