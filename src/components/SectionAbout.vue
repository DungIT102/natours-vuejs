<script setup></script>

<template>
  <section class="section-about">
    <div class="u-center-text u-margin-bottom-big">
      <h2 class="heading-secondary">Exciting tours for adventurous people</h2>
    </div>

    <div class="row">
      <div class="col-1-of-2 description">
        <h3 class="heading-tertiary u-margin-bottom-small">
          You're going to fall in love with nature
        </h3>
        <p class="paragraph">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente
          aspernatur libero repellat quis consequatur ducimus quam nisi exercitationem omnis earum
          qui.
        </p>

        <h3 class="heading-tertiary u-margin-bottom-small">
          Live adventures like you never have before
        </h3>
        <p class="paragraph">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores nulla deserunt
          voluptatum nam.
        </p>

        <a href="#" class="btn-text">Learn more &rarr;</a>
      </div>

      <div class="col-1-of-2">
        <div class="composition">
          <img
            srcset="@/assets/img/nat-1.jpg 300w, @/assets/img/nat-1-large.jpg 1000w"
            sizes="(max-width: 56.25rem) 20vw, (max-width: 37.5rem) 30vw, 300px"
            alt="photo 1"
            src="@/assets/img/nat-1-large.jpg"
            class="composition__photo composition__photo--p1"
          />

          <img
            srcset="@/assets/img/nat-2.jpg 300w, @/assets/img/nat-2-large.jpg 1000w"
            sizes="(max-width: 56.25rem) 20vw, (max-width: 37.5rem) 30vw, 300px"
            alt="photo 2"
            src="@/assets/img/nat-2-large.jpg"
            class="composition__photo composition__photo--p2"
          />

          <img
            srcset="@/assets/img/nat-3.jpg 300w, @/assets/img/nat-3-large.jpg 1000w"
            sizes="(max-width: 56.25rem) 20vw, (max-width: 37.5rem) 30vw, 300px"
            alt="photo 3"
            src="@/assets/img/nat-3-large.jpg"
            class="composition__photo composition__photo--p3"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .section-about {
    padding: 25rem 0;
    margin-top: -14vh;
    background-color: var(--color-grey-light-1);

    @media only screen and (max-width: $bp-md) {
      padding: 20rem 0;
    }

    .paragraph {
      font-size: var(--default-font-size);

      &:not(:last-child) {
        margin-bottom: 3rem;
      }
    }
  }

  /* sometimes &__element:hover not working with all specificity rules. Need break out to styles */
  .composition {
    position: relative;

    &__photo {
      width: 55%;
      border-radius: 2px;
      box-shadow: 0 1.5rem 4rem var(--shadow-color-04);

      position: absolute;
      z-index: 10;
      transition: all 0.3s;
      outline-offset: 1.2rem;

      @media only screen and (max-width: $bp-md) {
        position: relative;
        float: left;
        width: 33.33333333%;

        outline-offset: 1rem;
        box-shadow: 0 1.5rem 3rem var(--shadow-color-02);
      }

      &--p1 {
        left: 0;
        top: -2rem;

        @media only screen and (max-width: $bp-md) {
          top: 0;
          transform: scale(1.2);
        }
      }

      &--p2 {
        right: 0;
        top: 2rem;

        @media only screen and (max-width: $bp-md) {
          top: -1.2rem;
          transform: scale(1.3);
          z-index: 12;
        }
      }

      &--p3 {
        left: 20%;
        top: 10rem;

        @media only screen and (max-width: $bp-md) {
          top: 0;
          left: 0;
          transform: scale(1.2);
        }
      }

      &:hover {
        outline: 1rem solid var(--color-primary);
        transform: scale(1.15) translateY(-0.5rem);
        box-shadow: 0 2.5rem 4rem var(--shadow-color-05);
        z-index: 20;
      }
    }

    &:hover &__photo:not(img:hover) {
      transform: scale(0.95);
    }
  }
</style>
