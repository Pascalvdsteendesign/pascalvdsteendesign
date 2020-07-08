<template>
<div class="navigation">
    <a href="#" class="logo">
        <span>
            <img src="~/assets/img/logo.png">
        </span>
    </a>
    <ul class="link-list">
        <li>
            <a target="_blank" href="mailto:hello@pascalvdsteen.com" class="border-b">contact</a>
        </li>
    </ul>
</div>
</template>

<style lang="scss" scoped>
.navigation {
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: 2rem;

  @include respond-to(md) {
    padding-right: 5rem;
    height: 100px;
  }

  .logo {
    position: absolute;
    top: 0.5rem;
    left: 1.5rem;

    img {
      width: 50px;

      @include respond-to(md) {
        width: 80px;
      }
    }
  }

  .link-list {
    a {
      color: $color-primary;
      font-weight: $font-weight-bold;
      transition: ease 150ms;
      opacity: 0.5;

      &:hover {
        opacity: 1;
      }
    }
  }
}
</style>
