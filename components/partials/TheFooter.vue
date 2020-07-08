<template>
<footer class=" footer">
 <div class="contact">
   <h2>U heeft een vraag?</h2>
   <div class="h4">Mail dan naar  <a target="_blank" href="mailto:hello@pascalvdsteen.com" class="border-b">info@pascalvdsteen.com</a></div>
   <div class="icons">
            <a target="_blank" href="https://www.linkedin.com/in/pascal-v-a453578a">
                <span>
                    <img src="~/assets/img/icon-linkedin-white.svg">
                </span>

            </a>
            <a target="_blank" href="mailto:hello@pascalvdsteen.com">
                <span>
                    <img src="~/assets/img/icon-mail-white.svg">
                </span>
            </a>
             <a target="_blank" href="https://www.instagram.com/psvdsteen">
                <span>
                    <img src="~/assets/img/icon-instagram-white.svg">
                </span>
            </a>
            <a target="_blank" href="https://www.facebook.com/Pascal-van-der-Steen-design-251418652228243/">
                <span>
                    <img src="~/assets/img/icon-facebook-2-white.svg">
                </span>
            </a>
        </div>
 </div>
 
</footer>
</template>

<script>
</script>

<style lang="scss" scoped>
.contact {
  width: 80%;
  background-color: $color-black;
  margin: 4rem 0;
  padding: 3rem 2rem 5rem 2rem;

  h2,
  div,
  a {
    color: white;
  }

  a {
    opacity: 0.5;
    text-decoration: none;
    font-size: 1.5rem;

    &:hover {
      opacity: 1;
    }
  }

  .icons {
    margin-top: 1rem;

    @include respond-to(md) {
      margin-top: 0rem;
    }

    a {
      padding-right: 1rem;
      opacity: 0.5;

      transition: ease 250ms;

      &:hover {
        opacity: 1;
      }

      img {
        width: 20px;
      }

      &:nth-child(4) img {
        width: 12px;
      }
    }
  }
}
</style>
