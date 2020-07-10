<template>
<section class="container header">
    <div class="title">
        <h1>
            Front-end developer,<br> met passie voor UX-design
        </h1>
        <p>Hi, ik ben Pascal. Ik ontwikkel & design websites en<br> webapplicaties, waarbij de gebruikerservaring <br>altijd centraal staat.</p>
    </div>

    <div class="detail">
        <span class="h3 border-b">Details</span>
        <div class="icons">
            <a target="_blank" href="https://www.linkedin.com/in/pascal-van-der-steen-a453578a/">
                <span>
                    <img src="~/assets/img/icon-linkedin.svg">
                </span>

            </a>
            <a target="_blank" href="mailto:hello@pascalvdsteen.com">
                <span style="font-size: 1.2em; color: rgb(255, 157, 118);;">
                    <img src="~/assets/img/icon-mail.svg">
                </span>
            </a>
            <a target="_blank" href="https://www.instagram.com/psvdsteen">
                <span>
                    <img src="~/assets/img/icon-instagram.svg">
                </span>
            </a>
            <a target="_blank" href="https://www.facebook.com/Pascal-van-der-Steen-design-251418652228243/">
                <span>
                    <img src="~/assets/img/icon-facebook-2.svg">
                </span>
            </a>
        </div>
        <div class="info">
            <div class="item">
                <div class="h4">Functie</div>
                <div class="small-font">Front-end developer</div>
            </div>
            <div class="item">
                <div class="h4">Leeftijd</div>
                <div class="small-font">24</div>
            </div>
            <div class="item">
                <div class="h4">Gevestigd</div>
                <div class="small-font">Reijmerstok</div>
            </div>

        </div>
        <div class="clock-wrapper">
            <a target="_blank" href="mailto:hello@pascalvdsteen.com?subject=Tijd voor een nieuwe website">
                <TheClock></TheClock>
            </a>
        </div>
    </div>
</section>
</template>

<script>
import TheClock from "~/components/TheClock.vue";

export default {
  components: {
    TheClock
  }
};
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  flex-direction: column;
  margin-top: 2rem;
  margin-bottom: 2rem;
  padding-bottom: 2rem;
  overflow: hidden;

  @include respond-to(md) {
    margin-top: 2rem;
    overflow: unset;
  }

  @include respond-to(xl) {
    flex-direction: row;
    margin-top: 5rem;
  }

  .h3 {
    padding-right: 5rem;
  }

  .detail {
    position: relative;
    height: 350px;
    padding: 2rem 0 0 3rem;
    margin-top: 1rem;
    border: solid 5px $color-primary;

    @include respond-to(md) {
      width: 550px;
      height: 280px;
    }

    @include respond-to(xl) {
      margin-top: 0rem;
      margin-left: -6rem;
      width: 550px;
      height: 280px;
    }

    &:after {
      content: "";
      position: absolute;
      left: 1rem;
      top: 1rem;
      height: 100%;
      width: 100%;
      border: solid 5px $color-primary;
      opacity: 0.2;
      filter: blur(3px);
      pointer-events: none;
    }

    .icons {
      position: absolute;
      left: 3rem;
      top: 5rem;

      @include respond-to(md) {
        left: unset;
        right: 1rem;
        top: 2rem;
      }

      a {
        padding-right: 1rem;
        opacity: 0.5;
        transition: ease 250ms;

        &:hover {
          opacity: 1;
        }
      }
    }

    .info {
      position: absolute;
      bottom: 1rem;
      left: 3rem;
      display: flex;
      flex-direction: column;
      padding-right: 3rem;

      @include respond-to(md) {
        flex-direction: row;
      }

      .item {
        padding-right: 2rem;
        padding-bottom: 1rem;

        .h4 {
          line-height: 2;
        }

        .small-font {
          line-height: 1 !important;
        }
      }
    }

    .clock-wrapper {
      position: absolute;
      bottom: 1rem;
      right: 1rem;
    }
  }
}
</style>
