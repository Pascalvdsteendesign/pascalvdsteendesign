<template>
  <footer class=" footer">
    <div class="contact">
      <h2>Waar kan ik je mee helpen?</h2>
      <div class="h4">
        Neem contact op:<a
          target="_blank"
          href="mailto:hello@pascalvdsteen.com"
          class="border-b"
          >info@pascalvdsteen.com</a
        >
      </div>
      <div class="icons">
        <a
          target="_blank"
          href="https://www.linkedin.com/in/pascal-van-der-steen-a453578a/"
        >
          <span>
            <img
              src="~/assets/img/icon-linkedin-white.svg"
              alt="linkedin-icon"
            />
          </span>
        </a>
        <a target="_blank" href="mailto:hello@pascalvdsteen.com">
          <span>
            <img src="~/assets/img/icon-mail-white.svg" alt="email-icon" />
          </span>
        </a>
        <a target="_blank" href="https://www.instagram.com/psvdsteen">
          <span>
            <img
              src="~/assets/img/icon-instagram-white2.svg"
              alt="instagram-icon"
            />
          </span>
        </a>
        <a
          target="_blank"
          href="https://www.facebook.com/Pascal-van-der-Steen-design-251418652228243/"
        >
          <span>
            <img src="~/assets/img/icon-fb.svg" alt="facebook-icon" />
          </span>
        </a>
      </div>
    </div>
  </footer>
</template>

<script></script>

<style lang="scss" scoped>
.contact {
  width: 80%;
  background-color: $color-black;
  margin: 4rem 0;
  padding: 3rem 2rem 5rem 2rem;

  @include respond-to(md) {
    width: 80%;
  }

  .h4 a {
    margin-left: 1rem;
  }

  h2,
  div,
  a {
    color: white;
  }

  a {
    opacity: 0.5;
    text-decoration: none;
    font-size: 1rem;

    @include respond-to(sm) {
      font-size: 1.5rem;
    }
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
