<script setup></script>

<template>
  <section class="section-tours" id="section-tours">
    <div class="u-center-text u-margin-bottom-big">
      <h2 class="heading-secondary">Most popular tours</h2>
    </div>

    <div class="row">
      <div class="col-1-of-3">
        <div class="card">
          <div class="card__side card__side--front">
            <div class="card__picture card__picture--1">&nbsp;</div>
            <h4 class="card__heading">
              <span class="card__heading-span card__heading-span--1">The Sea Explorer</span>
            </h4>
            <div class="card__details">
              <ul>
                <li>3 day tours</li>
                <li>Up to 30 people</li>
                <li>2 tour guides</li>
                <li>Sleep in cozy hotels</li>
                <li>Difficulty: easy</li>
              </ul>
            </div>
          </div>
          <div class="card__side card__side--back card__side--back-1">
            <div class="card__cta">
              <div class="card__price-box">
                <p class="card__price-only">Only</p>
                <p class="card__price-value">$297</p>
              </div>
              <a href="#popup" class="btn btn--white">Book now!</a>
            </div>
          </div>
        </div>
      </div>

      <div class="col-1-of-3">
        <div class="card">
          <div class="card__side card__side--front">
            <div class="card__picture card__picture--2">&nbsp;</div>
            <h4 class="card__heading">
              <span class="card__heading-span card__heading-span--2">The Forest Hiker</span>
            </h4>
            <div class="card__details">
              <ul>
                <li>7 day tours</li>
                <li>Up to 40 people</li>
                <li>6 tour guides</li>
                <li>Sleep in provided tents</li>
                <li>Difficulty: medium</li>
              </ul>
            </div>
          </div>
          <div class="card__side card__side--back card__side--back-2">
            <div class="card__cta">
              <div class="card__price-box">
                <p class="card__price-only">Only</p>
                <p class="card__price-value">$497</p>
              </div>
              <a href="#popup" class="btn btn--white">Book now!</a>
            </div>
          </div>
        </div>
      </div>

      <div class="col-1-of-3">
        <div class="card">
          <div class="card__side card__side--front">
            <div class="card__picture card__picture--3">&nbsp;</div>
            <h4 class="card__heading">
              <span class="card__heading-span card__heading-span--3">The Snow Adventurer</span>
            </h4>
            <div class="card__details">
              <ul>
                <li>5 day tours</li>
                <li>Up to 15 people</li>
                <li>3 tour guides</li>
                <li>Sleep in provided tents</li>
                <li>Difficulty: hard</li>
              </ul>
            </div>
          </div>
          <div class="card__side card__side--back card__side--back-3">
            <div class="card__cta">
              <div class="card__price-box">
                <p class="card__price-only">Only</p>
                <p class="card__price-value">$897</p>
              </div>
              <a href="#popup" class="btn btn--white">Book now!</a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="u-center-text u-margin-top-huge">
      <a href="#" class="btn btn--green">Discover all tours</a>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .section-tours {
    padding: 25rem 0 15rem 0;
    margin-top: -10rem;
    background-color: var(--color-grey-light-1);

    @media only screen and (max-width: $bp-md) {
      padding: 20rem 0 10rem 0;
    }
  }

  /* Card */
  .card {
    position: relative;
    height: 52rem;
    perspective: 150rem;
    -moz-perspective: 150rem;

    &__side {
      width: 100%;
      height: 52rem;
      border-radius: 3px;
      transition: all 0.8s ease;

      position: absolute;
      top: 0;
      left: 0;
      overflow: hidden;

      -webkit-backface-visibility: hidden;
      backface-visibility: hidden;
      box-shadow: 0 1.5rem 4rem var(--shadow-color-015);

      &--front {
        background-color: var(--color-white);
      }

      &--back {
        transform: rotateY(180deg);

        &-1 {
          background-image: linear-gradient(
            to right bottom,
            var(--color-secondary-light),
            var(--color-secondary-dark)
          );
        }

        &-2 {
          background-image: linear-gradient(
            to right bottom,
            var(--color-primary-light),
            var(--color-primary-dark)
          );
        }

        &-3 {
          background-image: linear-gradient(
            to right bottom,
            var(--color-tertiary-light),
            var(--color-tertiary-dark)
          );
        }
      }
    }

    /* How it works with hover */
    &:hover &__side--front {
      transform: rotateY(-180deg);
    }

    &:hover &__side--back {
      transform: rotateY(0);
    }

    /* style for front side */
    &__picture {
      height: 23rem;
      border-top-left-radius: 3px;
      border-top-right-radius: 3px;

      background-size: cover;
      background-blend-mode: screen;
      -webkit-clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
      clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);

      &--1 {
        background-image: linear-gradient(
            to right bottom,
            var(--color-secondary-light),
            var(--color-secondary-dark)
          ),
          url(../assets/img/nat-5.jpg);
      }

      &--2 {
        background-image: linear-gradient(
            to right bottom,
            var(--color-primary-light),
            var(--color-primary-dark)
          ),
          url(../assets/img/nat-6.jpg);
      }

      &--3 {
        background-image: linear-gradient(
            to right bottom,
            var(--color-tertiary-light),
            var(--color-tertiary-dark)
          ),
          url(../assets/img/nat-7.jpg);
      }
    }

    &__heading {
      position: absolute;
      top: 12rem;
      right: 2rem;
      width: 75%;

      font-size: 2.8rem;
      font-weight: 300;
      text-align: right;
      text-transform: uppercase;

      color: var(--color-white);
    }

    &__heading-span {
      padding: 1rem 1.5rem;
      -webkit-box-decoration-break: clone;
      box-decoration-break: clone;

      &--1 {
        background-image: linear-gradient(
          to right bottom,
          var(--color-secondary-light),
          var(--color-secondary-dark)
        );
      }

      &--2 {
        background-image: linear-gradient(
          to right bottom,
          var(--color-primary-light),
          var(--color-primary-dark)
        );
      }

      &--3 {
        background-image: linear-gradient(
          to right bottom,
          var(--color-tertiary-light),
          var(--color-tertiary-dark)
        );
      }
    }

    &__details {
      padding: 3rem;

      ul {
        list-style: none;
        width: 80%;
        margin: 0 auto;

        li {
          padding: 1rem;
          font-size: 1.5rem;
          text-align: center;

          &:not(:last-child) {
            border-bottom: 1px solid var(--color-grey-light-2);
          }
        }
      }
    }

    /* style for back side */
    &__cta {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

      width: 90%;
      text-align: center;
    }

    &__price-box {
      margin-bottom: 8rem;
      color: var(--color-white);
      text-align: center;
    }

    &__price-only {
      font-size: 1.4rem;
      text-transform: uppercase;
    }

    &__price-value {
      font-size: 6rem;
      font-weight: 100;
    }

    /* make effect of card work only with some case */
    @media only screen and (max-width: $bp-md), only screen and (hover: none) {
      height: auto;
      border-radius: 3px;
      background-color: var(--color-white);
      box-shadow: 0 1.5rem 4rem var(--shadow-color-015);

      &__side {
        position: relative;
        height: auto;
        box-shadow: none;

        &--back {
          transform: rotateY(0);
          clip-path: polygon(0 15%, 100% 0, 100% 100%, 0 100%);
          -webkit-clip-path: polygon(0 15%, 100% 0, 100% 100%, 0 100%);
        }
      }

      &:hover &__side--front {
        transform: rotateY(0);
      }

      &__details {
        padding: 1rem 3rem;
      }

      /* style for back side */
      &__cta {
        position: relative;
        top: 0;
        left: 0;
        transform: translate(0);

        width: 100%;
        padding: 7rem 4rem 4rem 4rem;
      }

      &__price-box {
        margin-bottom: 3rem;
      }

      &__price-value {
        font-size: 4rem;
      }
    }
  }
</style>
