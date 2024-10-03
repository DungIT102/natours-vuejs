<script setup></script>

<template>
  <footer class="footer">
    <div class="footer__logo-box">
      <picture class="footer__logo">
        <source
          srcset="@/assets/img/logo-green-small-1x.png 1x, @/assets/img/logo-green-small-2x.png 2x"
          media="(max-width: 37.5rem)"
        />
        <img
          srcset="@/assets/img/logo-green-1x.png 1x, @/assets/img/logo-green-2x.png 2x"
          alt="Full logo"
          src="@/assets/img/logo-green-2x.png"
        />
      </picture>
    </div>
    <div class="row">
      <div class="col-1-of-2">
        <div class="footer__navigation">
          <ul class="footer__list">
            <li class="footer__item"><a href="#" class="footer__link">Company</a></li>
            <li class="footer__item"><a href="#" class="footer__link">Contact us</a></li>
            <li class="footer__item"><a href="#" class="footer__link">Carrers</a></li>
            <li class="footer__item"><a href="#" class="footer__link">Privacy policy</a></li>
            <li class="footer__item"><a href="#" class="footer__link">Terms</a></li>
          </ul>
        </div>
      </div>
      <div class="col-1-of-2">
        <p class="footer__copyright">Copyright &copy; by Le Dung</p>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
  .footer {
    font-size: 1.4rem;
    padding: 10rem 0;
    color: var(--color-grey-light-1);
    background-color: var(--color-grey-dark-3);

    @media only screen and (max-width: $bp-md) {
      padding: 8rem 0;
    }

    &__logo-box {
      text-align: center;
      margin-bottom: 8rem;

      @media only screen and (max-width: $bp-md) {
        margin-bottom: 6rem;
      }
    }

    &__logo {
      width: 12rem;
      height: auto;
    }

    &__list {
      list-style: none;
    }

    &__navigation {
      display: inline-block;
      padding-top: 2rem;
      border-top: 1px solid var(--color-grey-dark);

      @media only screen and (max-width: $bp-md) {
        width: 100%;
        text-align: center;
      }
    }

    &__item {
      display: inline-block;

      &:not(:last-child) {
        margin-right: 1.5rem;
      }
    }

    &__link {
      &:link,
      &:visited {
        display: inline-block;
        text-decoration: none;
        text-transform: uppercase;

        color: var(--color-grey-light-1);
        background-color: var(--color-grey-dark-3);
        transition: all 0.2s;
      }

      &:hover,
      &:active {
        color: var(--color-primary);
        box-shadow: 0 1rem 2rem var(--shadow-color-04);
        transform: rotate(5deg) scale(1.3);
      }
    }

    &__copyright {
      width: 80%;
      float: right;
      padding-top: 2rem;
      border-top: 1px solid var(--color-grey-dark);

      @media only screen and (max-width: $bp-md) {
        width: 100%;
        float: none;
      }
    }
  }
</style>
