<template>
<div class="navigation">
    <a href="#" class="logo">
        <span>
            <img src="~/assets/img/logo.svg">
        </span>
    </a>
    <ul class="link-list">
        <li>
            <a target="_blank" href="mailto:pascalvdsteen@hotmail.com" class="border-b">contact</a>
        </li>
    </ul>
</div>
</template>

<style lang="scss" scoped>
.navigation {
    height: 150px;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding-right: 5rem;

    .logo {
        position: absolute;
        top: 1rem;
        left: 1rem;
    }

    .link-list {
        a {
            color: $color-primary;
            font-weight: $font-weight-bold;
            transition: ease 150ms;

        }
    }

}
</style>
