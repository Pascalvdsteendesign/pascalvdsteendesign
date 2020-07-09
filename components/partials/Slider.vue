<template>
<section class="container projects">
    <div class="my-slider">
        <VueSlickCarousel v-bind="settings">
            <div class="thumb">
                <a target="_blank" href="https://www.byldis.com/">
                    <div class="bg-image" :style="{ 'background-image': 'url(' + require('~/assets/img/byldis.jpg') + ')' }"> </div>
                    <div class="thumb-inner">
                        <div class="h5">Development</div>
                        <div class="h3 border-b">Byldis<div class="h6">In opdracht van Nexwork</div>
                        </div>
                        <div href="#" class="h5">Bekijk de website</div>
                    </div>
                </a>
            </div>
               <div class="thumb">
                <a target="_blank" href="https://minor-education-test.netlify.app/">
                    <div class="bg-image" :style="{ 'background-image': 'url(' + require('~/assets/img/monitor.jpg') + ')' }"> </div>
                    <div class="thumb-inner">
                        <div class="h5">Development (PWA)</div>
                        <div class="h3 border-b">Leerling monitor<div class="h6">Vraag naar meer info</div>
                        </div>
                        <div href="#" class="h5">Bekijk de website</div>
                    </div>
                </a>
            </div>
            <div class="thumb">
                <a target="_blank" href="https://www.thanda-ecologischcentrum.nl/">
                    <div class="bg-image" :style="{ 'background-image': 'url(' + require('~/assets/img/thanda.jpg') + ')' }"> </div>
                    <div class="thumb-inner">
                        <div class="h5">Development & design</div>
                        <div class="h3 border-b">Thanda <br>ECB</div>
                        <div href="#" class="h5">Bekijk de website</div>
                    </div>
                </a>
            </div>
            <div class="thumb">
                <a target="_blank" href="https://www.mondanifarm.com/">
                    <div class="bg-image" :style="{ 'background-image': 'url(' + require('~/assets/img/mondani.jpg') + ')' }"> </div>
                    <div class="thumb-inner">
                        <div class="h5">Development & design</div>
                        <div class="h3 border-b">Mondani<br> Farm</div>
                        <div href="#" class="h5">Bekijk de website</div>
                    </div>
                </a>
            </div>

            <div class="thumb">
                <a target="_blank" href="https://hoeve-doodleger.netlify.app/">
                    <div class="bg-image" :style="{ 'background-image': 'url(' + require('~/assets/img/hoeve.png') + ')' }"> </div>
                    <div class="thumb-inner">
                        <div class="h5">Development & design</div>
                        <div class="h3 border-b">Hoeve<br> doodleger</div>
                        <div href="#" class="h5">Bekijk de website</div>
                    </div>
                </a>
            </div>
            <div class="thumb">
                <a target="_blank" href="mailto:hello@pascalvdsteen.com">
                    <div class="bg-image" :style="{ 'background-image': 'url(' + 'https://images.unsplash.com/photo-1554050857-c84a8abdb5e2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=882&q=80' + ')' }"> </div>
                    <div class="thumb-inner">
                        <div class="h5">Contact</div>
                        <div class="h3 border-b">Uw project<br> hier?</div>
                        <div href="#" class="h5">Stel een vraag</div>
                    </div>
                </a>
            </div>
        </VueSlickCarousel>
        <div class="blur">
        </div>
    </div>
</section>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  data() {
    return {
      settings: {
        infinite: true,
        speed: 600,
        slidesToShow: 4,
        slidesToScroll: 1,
        initialSlide: 0,
        pauseOnHover: true,
        responsive: [
          {
            breakpoint: 992,
            settings: {
              slidesToShow: 3,
              slidesToScroll: 1
            }
          },
          {
            breakpoint: 767,
            settings: {
              slidesToShow: 2,
              slidesToScroll: 1
            }
          },
          {
            breakpoint: 575,
            settings: {
              slidesToShow: 1,
              slidesToScroll: 1
            }
          }
        ]
      }
    };
  },

  components: {
    VueSlickCarousel
  }
};
</script>

<style lang="scss">
.projects {
  position: relative;
  height: 500px;
  overflow: hidden;

  @include respond-to(xl) {
    margin-top: -1rem;
  }

  .slick-slider {
    display: table !important;
    table-layout: fixed !important;
    width: 100% !important;
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
    .h6,
    a {
      color: $color-secondary;
    }

    .border-b {
      border-bottom: solid 5px $color-secondary;
    }
  }

  .slick-next {
    position: absolute;
    right: 3rem;
    top: 25rem;
    z-index: 9;

    @include respond-to(sm) {
      right: 12rem;
      top: 11rem;
    }

    &:before {
      font-size: 50px;
      color: $color-primary;
    }

    @include respond-to(md) {
      right: 7rem;
    }

    @include respond-to(lg) {
      right: 10rem;
    }

    @include respond-to(xl) {
      right: 12rem;
    }
  }

  .my-slider {
    position: relative;

    .blur {
      display: none;
      position: absolute;
      right: -0.5rem;
      top: 0;
      background: $color-secondary;
      width: calc(100% / 2);
      height: 110%;
      opacity: 0.96;
      filter: blur(12px);
      -webkit-filter: blur(8px);

      @include respond-to(sm) {
        display: block;
        width: calc(100% / 2);
      }

      @include respond-to(md) {
        width: calc(100% / 3);
      }

      @include respond-to(lg) {
        width: calc(100% / 4);
      }
    }

    .thumb {
      position: relative;
      height: 380px;
      width: 100% !important;

      @include respond-to(sm) {
        height: 480px;
      }

      .bg-image {
        position: absolute;
        height: 100%;
        width: 100%;
        background-size: cover;
        background-position: center;
        opacity: 0;
        transition: ease 300ms;

        &:after {
          content: "";
          position: absolute;
          width: 100%;
          height: 100%;
          top: 0;
          left: 0;
          background: rgba(0, 0, 0, 0.7);
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

        .h6 {
          font-size: 16px;
          margin-top: 0.6rem;
        }

        .h5 {
          line-height: 1.2;
          margin-top: 1.25rem;
          margin-bottom: 1rem;
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
        .h6 {
          color: $color-secondary !important;
        }

        a {
          color: $color-secondary !important;
        }

        .border-b {
          border-bottom: solid 5px $color-secondary;
        }
      }

      &:hover ~ .slick-current .bg-image {
        opacity: 0 !important;
      }
    }
  }
}
</style>
