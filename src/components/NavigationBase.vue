<script setup></script>

<template>
  <section class="navigation">
    <input type="checkbox" class="navigation__checkbox" id="navi-toggle" />
    <label for="navi-toggle" class="navigation__button">
      <span class="navigation__icon">&nbsp;</span>
    </label>

    <div class="navigation__background">&nbsp;</div>

    <nav class="navigation__nav">
      <ul class="navigation__list">
        <li class="navigation__item">
          <a href="#" class="navigation__link"><span>01</span>About Natours</a>
        </li>
        <li class="navigation__item">
          <a href="" class="navigation__link"><span>02</span>Your benefits</a>
        </li>
        <li class="navigation__item">
          <a href="" class="navigation__link"><span>03</span>Popular tours</a>
        </li>
        <li class="navigation__item">
          <a href="" class="navigation__link"><span>04</span>Stories</a>
        </li>
        <li class="navigation__item">
          <a href="" class="navigation__link"><span>05</span>Book now</a>
        </li>
      </ul>
    </nav>
  </section>
</template>

<style lang="scss" scoped>
  .navigation {
    /* Button with checkbox */
    &__checkbox {
      display: none;
    }

    &__button {
      width: 7rem;
      height: 7rem;
      background-color: var(--color-white);
      box-shadow: 0 1rem 3rem var(--shadow-color-01);

      position: fixed;
      top: 6rem;
      right: 6rem;
      border-radius: 50%;

      cursor: pointer;
      z-index: 1500;
      text-align: center;

      @media only screen and (max-width: $bp-md) {
        top: 4rem;
        right: 4rem;
      }

      @media only screen and (max-width: $bp-sm) {
        top: 3rem;
        right: 3rem;
      }
    }

    /* Create icon button */
    &__icon {
      position: relative;
      margin-top: 3.5rem;

      &,
      &::before,
      &::after {
        display: inline-block;
        width: 3rem;
        height: 2px;
        background-color: var(--color-grey-dark-3);
      }

      &::before,
      &::after {
        content: '';
        position: absolute;
        left: 0;
        transition:
          top 0.1s,
          transform 0.2s;
      }

      &::before {
        top: -0.8rem;
      }

      &::after {
        top: 0.8rem;
      }
    }

    /* How to button works */
    &__button:hover &__icon::before {
      top: -1rem;
    }

    &__button:hover &__icon::after {
      top: 1rem;
    }

    &__checkbox:checked + &__button &__icon::before {
      top: 0;
      transform: rotate(135deg);
    }

    &__checkbox:checked + &__button &__icon::after {
      top: 0;
      transform: rotate(-135deg);
    }

    &__checkbox:checked + &__button &__icon {
      background-color: transparent;
    }

    /* Create background */
    &__background {
      width: 6rem;
      height: 6rem;
      border-radius: 50%;

      position: fixed;
      top: 6.5rem;
      right: 6.5rem;
      z-index: 1000;

      background-image: radial-gradient(var(--color-primary-light), var(--color-primary-dark));
      transition: transform 0.8s cubic-bezier(0.86, 0, 0.07, 1);

      @media only screen and (max-width: $bp-md) {
        top: 4.5rem;
        right: 4.5rem;
      }

      @media only screen and (max-width: $bp-sm) {
        top: 3.5rem;
        right: 3.5rem;
      }
    }

    /* How to background works with checkbox */
    &__checkbox:checked ~ &__background {
      transform: scale(80);
    }

    /* nav and list item */
    &__nav {
      position: fixed;
      top: 0;
      left: -50%; /* let element not working with mount */
      height: 100vh;

      opacity: 0;
      width: 0;
      z-index: 1500;
      transition: all 0.8s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    }

    &__list {
      position: absolute;
      top: 50%;
      left: 100%; /* normal value is 50% but &__nav left is -50% so it will be 50% */
      transform: translate(-50%, -50%);

      width: 100%;
      list-style: none;
      text-align: center;
    }

    &__item {
      margin: 1rem;
    }

    /* How to nav works with checkbox */
    &__checkbox:checked ~ &__nav {
      opacity: 1;
      width: 100%;
    }

    /* link */
    &__link {
      &:link,
      &:visited {
        display: inline-block;
        font-size: 3rem;
        font-weight: 300;
        padding: 1rem 2rem;

        color: var(--color-white);
        text-decoration: none;
        text-transform: uppercase;

        background-image: linear-gradient(
          120deg,
          transparent 0%,
          transparent 50%,
          var(--color-white) 50%
        );
        background-size: 220%;
        transition: all 0.4s;

        span {
          display: inline-block;
          margin-right: 1.5rem;
        }
      }

      &:hover,
      &:active {
        background-position: 100%;
        color: var(--color-primary);
        transform: translateX(1rem);
      }
    }
  }
</style>
