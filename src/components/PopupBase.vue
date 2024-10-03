<script setup></script>

<template>
  <section class="popup" id="popup">
    <div class="popup__content">
      <div class="popup__left">
        <img src="@/assets/img/nat-8.jpg" alt="Tour photo" class="popup__img" />
        <img src="@/assets/img/nat-9.jpg" alt="Tour photo" class="popup__img" />
      </div>
      <div class="popup__right">
        <a href="#section-tours" class="popup__close">&times;</a>
        <h2 class="heading-secondary u-margin-bottom-small">Start booking now</h2>
        <h3 class="heading-tertiary u-margin-bottom-small">
          Important &ndash; Please read these terms before booking
        </h3>
        <p class="popup__text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
          ut labore et dolore magna aliqua. Sed sed risus pretium quam. Aliquam sem et tortor
          consequat id. Volutpat odio facilisis mauris sit amet massa vitae. Mi bibendum neque
          egestas congue. Placerat orci nulla pellentesque dignissim enim sit. Vitae semper quis
          lectus nulla at volutpat diam ut venenatis. Malesuada pellentesque elit eget gravida cum
          sociis natoque penatibus et. Proin fermentum leo vel orci porta non pulvinar neque
          laoreet. Gravida neque convallis a cras semper.
        </p>
        <a href="#" class="btn btn--green">Book now</a>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .popup {
    position: fixed;
    top: 0;
    left: 0;

    width: 100%;
    height: 100vh;
    z-index: 9999;

    opacity: 0;
    visibility: hidden;
    transition: all 0.3s;
    background-color: var(--b-color-black-08);

    @supports (-webkit-backdrop-filter: blur(10px)) or (backdrop-filter: blur(10px)) {
      -webkit-backdrop-filter: blur(10px);
      backdrop-filter: blur(10px);
      background-color: var(--b-color-black-03);
    }

    &__content {
      position: absolute;
      top: 50%;
      left: 50%;
      opacity: 0;

      display: table;
      width: 75%;
      border-radius: 3px;
      overflow: hidden;

      background-color: var(--color-white);
      box-shadow: 0 2rem 4rem var(--shadow-color-02);
      transform: translate(-50%, -50%) scale(0.25);
      transition: all 0.5s 0.2s;
    }

    &__left {
      display: table-cell;
      width: 33.333333%;

      @media only screen and (max-width: $bp-md) {
        display: none;
      }
    }

    &__right {
      display: table-cell;
      width: 66.666667%;
      padding: 3rem 5rem;
      vertical-align: middle;

      @media only screen and (max-width: $bp-md) {
        width: 100%;
      }

      a:not(a:first-child) {
        float: right;
      }
    }

    &__img {
      display: block;
      width: 100%;
    }

    &__text {
      font-size: 1.4rem;
      margin-bottom: 4rem;
      hyphens: auto;

      column-count: 2;
      column-gap: 4rem;
      column-rule: 1px solid var(--color-grey-light-2);

      @media only screen and (max-width: $bp-md) {
        column-count: 1;
      }
    }

    &__close {
      display: inline-block;
      position: absolute;
      top: 2.5rem;
      right: 2.5rem;

      font-size: 3rem;
      line-height: 1;
      text-decoration: none;

      color: var(--color-grey-dark);
      transition: all 0.2s;

      &:hover {
        color: var(--color-primary);
      }
    }

    /* Animation for popup */
    &:target {
      opacity: 1;
      visibility: visible;
    }

    &:target &__content {
      opacity: 1;
      transform: translate(-50%, -50%) scale(1);
    }
  }
</style>
