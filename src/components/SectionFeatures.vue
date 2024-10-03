<script setup></script>

<template>
  <section class="section-features">
    <div class="row">
      <div class="col-1-of-4">
        <div class="feature-box">
          <i class="feature-box__icon icon-basic-world"></i>
          <h3 class="heading-tertiary u-margin-bottom-small">Explore the world</h3>
          <p class="feature-box__text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente
            aspernatur.
          </p>
        </div>
      </div>

      <div class="col-1-of-4">
        <div class="feature-box">
          <i class="feature-box__icon icon-basic-compass"></i>
          <h3 class="heading-tertiary u-margin-bottom-small">Meet nature</h3>
          <p class="feature-box__text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente
            aspernatur.
          </p>
        </div>
      </div>

      <div class="col-1-of-4">
        <div class="feature-box">
          <i class="feature-box__icon icon-basic-map"></i>
          <h3 class="heading-tertiary u-margin-bottom-small">Find your way</h3>
          <p class="feature-box__text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente
            aspernatur.
          </p>
        </div>
      </div>

      <div class="col-1-of-4">
        <div class="feature-box">
          <i class="feature-box__icon icon-basic-heart"></i>
          <h3 class="heading-tertiary u-margin-bottom-small">Live a healthier life</h3>
          <p class="feature-box__text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente
            aspernatur.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  /* setting new font to use */
  @charset 'UTF-8';
  @font-face {
    font-family: 'linea-basic-10';
    src: url('../assets/fonts/linea-basic-10.eot');
    src:
      url('../assets/fonts/linea-basic-10.eot?#iefix') format('embedded-opentype'),
      url('../assets/fonts/linea-basic-10.woff') format('woff'),
      url('../assets/fonts/linea-basic-10.ttf') format('truetype'),
      url('../assets/fonts/linea-basic-10.svg#linea-basic-10') format('svg');
    font-weight: normal;
    font-style: normal;
  }

  [class^='icon-']:before,
  [class*=' icon-']:before {
    font-family: 'linea-basic-10' !important;
    font-style: normal !important;
    font-weight: normal !important;
    font-variant: normal !important;
    text-transform: none !important;
    speak-as: none;
    line-height: 1;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  /* Section Features */
  .section-features {
    padding: 20rem 0;
    margin-top: -10rem;
    transform: skewY(-7deg);

    background-image: linear-gradient(
        to right bottom,
        var(--b-color-primary-light),
        var(--b-color-primary-dark)
      ),
      url('../assets/img/nat-4.jpg');

    background-size: cover;

    & > * {
      transform: skewY(7deg);
    }

    @media only screen and (max-width: $bp-md) {
      padding: 10rem 0;
    }
  }

  /* Feature Box */
  .feature-box {
    padding: 2.5rem;
    border-radius: 3px;
    box-shadow: 0 1.5rem 4rem var(--shadow-color-015);
    background-color: var(--b-color-white-08);

    font-size: 1.5rem;
    text-align: center;
    transition: transform 0.25s;

    @media only screen and (max-width: $bp-md) {
      padding: 2rem;
    }

    /* icon */
    .icon-basic-world::before {
      content: '\e028';
    }

    .icon-basic-compass::before {
      content: 'B';
    }

    .icon-basic-map::before {
      content: '+';
    }

    .icon-basic-heart::before {
      content: 'W';
    }

    &__icon {
      display: inline-block;
      margin-bottom: 0.5rem;

      font-size: 6rem;
      color: var(--b-color-primary-light);
      @supports (-webkit-background-clip: text) or (background-clip: text) {
        color: transparent;
        -webkit-background-clip: text;
        background-clip: text;
        background-image: linear-gradient(
          to right,
          var(--color-primary-light),
          var(--color-primary-dark)
        );
      }
    }

    &:hover {
      transform: translateY(-1.5rem) scale(1.03);
    }
  }
</style>
