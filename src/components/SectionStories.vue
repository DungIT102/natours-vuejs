<script setup></script>

<template>
  <section class="section-stories">
    <div class="bg-video">
      <video class="bg-video__content" autoplay muted loop>
        <source src="@/assets/img/video.mp4" type="video/mp4" />
        <source src="@/assets/img/video.webm" type="video/webm" />
        Your browser is not supported!
      </video>
    </div>

    <div class="u-center-text u-margin-bottom-big">
      <h2 class="heading-secondary">We make people genuinely happy</h2>
    </div>

    <div class="row">
      <div class="story">
        <figure class="story__shape">
          <img src="@/assets/img/nat-8.jpg" alt="Person a tours" class="story__img" />
          <figcaption class="story__caption">Mary Smith</figcaption>
        </figure>

        <div class="story__text">
          <div class="heading-tertiary u-margin-bottom-small">
            I had the best week ever with my family
          </div>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente
            aspernatur libero repellat quis consequatur ducimus quam nisi exercitationem omnis earum
            qui. Aperiam, ipsum sapiente aspernatur libero repellat quis consequatur ducimus quam
            nisi exercitationem omnis earum qui.
          </p>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="story">
        <figure class="story__shape">
          <img src="@/assets/img/nat-9.jpg" alt="Person on a tour" class="story__img" />
          <figcaption class="story__caption">Jack Wilson</figcaption>
        </figure>
        <div class="story__text">
          <h3 class="heading-tertiary u-margin-bottom-small">
            WOW! My life is completely different now
          </h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente
            aspernatur libero repellat quis consequatur ducimus quam nisi exercitationem omnis earum
            qui. Aperiam, ipsum sapiente aspernatur libero repellat quis consequatur ducimus quam
            nisi exercitationem omnis earum qui.
          </p>
        </div>
      </div>
    </div>

    <div class="u-center-text u-margin-top-huge">
      <a href="#" class="btn-text">Read all stories &rarr;</a>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .section-stories {
    position: relative;
    padding: 15rem 0;

    @media only screen and (max-width: $bp-md) {
      padding: 10rem 0;
    }
  }

  /* Background video */
  .bg-video {
    position: absolute;
    top: 0;
    left: 0;

    width: 100%;
    height: 100%;
    z-index: -1;

    opacity: 0.15;
    overflow: hidden;

    &__content {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }

  /* story */
  .story {
    width: 75%;
    margin: 0 auto;
    padding: 6rem 6rem 6rem 9rem;
    border-radius: 3px;

    font-size: var(--default-font-size);
    box-shadow: 0 3rem 6rem var(--shadow-color-01);
    background-color: var(--b-color-white-06);
    transform: skewX(-12deg);

    @media only screen and (max-width: $bp-md) {
      width: 100%;
      padding: 4rem 4rem 4rem 7rem;
    }

    @media only screen and (max-width: $bp-sm) {
      transform: skewX(0);
    }

    &__shape {
      width: 15rem;
      height: 15rem;
      float: left;

      position: relative;
      overflow: hidden;
      border-radius: 50%;
      transform: translateX(-3rem) skewX(12deg);

      @supports (clip-path: polygon(0 0)) or (-webkit-clip-path: polygon(0 0)) {
        -webkit-clip-path: circle(50% at 50% 50%);
        -webkit-shape-outside: circle(50% at 50% 50%);
        clip-path: circle(50% at 50% 50%);
        shape-outside: circle(50% at 50% 50%);
        border-radius: none;
      }

      @media only screen and (max-width: $bp-sm) {
        transform: translateX(-3rem) skewX(0);
      }
    }

    &__img {
      height: 100%;
      backface-visibility: hidden;
      transform: translateX(-4rem) scale(1.4);
      transition: all 0.5s;
    }

    &__caption {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, 20%);

      font-size: 1.7rem;
      text-align: center;
      text-transform: uppercase;

      color: var(--color-white);
      opacity: 0;
      backface-visibility: hidden;
      transition: all 0.5s;
    }

    &:hover &__caption {
      opacity: 1;
      transform: translate(-50%, -50%);
    }

    &:hover &__img {
      transform: translateX(-4rem) scale(1);
      filter: blur(3px) brightness(80%);
    }

    &__text {
      transform: skewX(12deg);

      @media only screen and (max-width: $bp-sm) {
        transform: skewX(0);
      }
    }
  }
</style>
