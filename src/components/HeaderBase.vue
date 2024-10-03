<script setup></script>

<template>
  <header class="header">
    <div class="header__logo-box">
      <img src="@/assets/img/logo-white.png" alt="logo" class="header__logo" />
    </div>

    <div class="header__text-box">
      <h1 class="heading-primary">
        <span class="heading-primary--main">Outdoors</span>
        <span class="heading-primary--sub">is where life happens</span>
      </h1>

      <a href="#" class="btn btn--white btn--animated">Discover our tours</a>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  .header {
    position: relative;
    height: 85vh;
    background-image: linear-gradient(
        to right bottom,
        var(--b-color-primary-light),
        var(--b-color-primary-dark)
      ),
      url(@/assets/img/hero-small.jpg);
    background-size: cover;
    background-position: top;

    /* add condition to use big image */
    @media only screen and (min-resolution: 192dpi) and (min-width: $bp-sm),
      only screen and (-webkit-min-device-pixel-ratio: 2) and (min-width: $bp-sm),
      only screen and (min-width: $bp-xxl) {
      background-image: linear-gradient(
          to right bottom,
          var(--b-color-primary-light),
          var(--b-color-primary-dark)
        ),
        url(@/assets/img/hero.jpg);
    }

    /* add condition to browser apply clip-path or not */
    @supports (clip-path: polygon(0 0)) or (-webkit-clip-path: polygon(0 0)) {
      -webkit-clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
      clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
      height: 95vh;
    }

    /* Logo */
    &__logo-box {
      position: absolute;
      top: 4rem;
      left: 4rem;
    }

    &__logo {
      height: 3.5rem;
    }

    /* Textbox */
    &__text-box {
      position: absolute;
      top: 40%;
      left: 50%;
      transform: translate(-50%, -50%);

      text-align: center;
    }
  }
</style>
