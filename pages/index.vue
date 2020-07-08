<template>
<div>
    <TheHeader />
    <Slider />
    <TheFooter />
</div>
</template>

<script>
import TheHeader from "~/components/partials/TheHeader.vue";
import Slider from "~/components/partials/Slider.vue";
import TheFooter from "~/components/partials/TheFooter.vue";

export default {
  components: {
    TheHeader,
    Slider,
    TheFooter
  }
};
</script>

<style lang="scss" scoped>
</style>
