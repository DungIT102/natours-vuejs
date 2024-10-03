<script setup></script>

<template>
  <section class="section-book">
    <div class="row">
      <div class="book">
        <div class="book__form">
          <form action="#" class="form">
            <div class="u-margin-bottom-medium">
              <h2 class="heading-secondary">Start booking now</h2>
            </div>

            <div class="form__group">
              <input type="text" class="form__input" placeholder="Full name" id="name" required />
              <label for="name" class="form__label">Full name</label>
            </div>

            <div class="form__group">
              <input
                type="email"
                class="form__input"
                placeholder="Email address"
                id="email"
                required
              />
              <label for="email" class="form__label">Email address</label>
            </div>

            <div class="form__group u-margin-bottom-medium">
              <div class="form__radio-group">
                <input type="radio" class="form__radio-input" id="small" name="size" />
                <label for="small" class="form__radio-label">
                  <span class="form__radio-button"></span>
                  Small tour group
                </label>
              </div>

              <div class="form__radio-group">
                <input type="radio" class="form__radio-input" id="large" name="size" />
                <label for="large" class="form__radio-label">
                  <span class="form__radio-button"></span>
                  Large tour group
                </label>
              </div>
            </div>

            <div class="form__group">
              <button class="btn btn--green">Next step &rarr;</button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .section-book {
    padding: 15rem 0;
    background-image: linear-gradient(
      to right bottom,
      var(--color-primary-light),
      var(--color-primary-dark)
    );

    @media only screen and (max-width: $bp-md) {
      padding: 10rem 0;
    }
  }

  /* Book */
  .book {
    border-radius: 3px;
    box-shadow: 0 1.5rem 4rem var(--shadow-color-02);
    background-image: linear-gradient(
        105deg,
        var(--b-color-white-09) 0%,
        var(--b-color-white-09) 50%,
        transparent 50%
      ),
      url(../assets/img/nat-10.jpg);
    background-size: 100%;

    @media only screen and (max-width: $bp-xl) {
      background-image: linear-gradient(
          105deg,
          var(--b-color-white-09) 0%,
          var(--b-color-white-09) 65%,
          transparent 65%
        ),
        url(../assets/img/nat-10.jpg);
      background-size: cover;
    }

    @media only screen and (max-width: $bp-md) {
      background-image: linear-gradient(
          to right,
          var(--b-color-white-09) 0%,
          var(--b-color-white-09) 100%
        ),
        url(../assets/img/nat-10.jpg);
    }

    &__form {
      width: 50%;
      padding: 6rem;

      @media only screen and (max-width: $bp-xl) {
        width: 65%;
      }

      @media only screen and (max-width: $bp-md) {
        width: 100%;
      }
    }
  }

  /* Form */
  .form {
    &__group:not(:last-child) {
      margin-bottom: 2rem;
    }

    &__input {
      display: block;
      width: 90%;
      padding: 1.5rem 2rem;

      border-radius: 2px;
      border: none;
      border-bottom: 3px solid transparent;

      font-size: 1.5rem;
      font-family: inherit;
      color: inherit;
      background-color: var(--b-color-white-05);
      transition: all 0.3s;

      @media only screen and (max-width: $bp-sm) {
        width: 100%;
      }

      &:focus {
        outline: none;
        box-shadow: 0 1rem 2rem var(--shadow-color-01);
        border-bottom: 3px solid var(--color-primary);
      }

      &:focus:invalid {
        border-bottom: 3px solid var(--color-secondary-dark);
      }

      &::-webkit-input-placeholder {
        color: var(--color-grey-dark-2);
      }
    }

    &__label {
      display: block;
      margin-left: 2rem;
      margin-top: 0.7rem;

      font-size: 1.2rem;
      font-weight: 700;
      transition: all 0.3s;
    }

    /* how to animate the label when the placeholder-shown */
    &__input:placeholder-shown + &__label {
      opacity: 0;
      visibility: hidden;
      transform: translateY(-4rem);
    }

    /* Radio button */

    &__radio-group {
      display: inline-block;
      width: 49%;

      @media only screen and (max-width: $bp-md) {
        width: 100%;
        margin-bottom: 2rem;
      }
    }

    /* Remove the default radio */
    &__radio-input {
      display: none;
    }

    &__radio-label {
      position: relative;
      padding-left: 4.5rem;

      font-size: var(--default-font-size);
      cursor: pointer;
    }

    /* Create the radio button */
    &__radio-button {
      display: inline-block;
      width: 3rem;
      height: 3rem;
      border: 5px solid var(--color-primary);
      border-radius: 50%;

      position: absolute;
      top: -0.4rem;
      left: 0;

      &::after {
        content: '';
        display: block;
        width: 1.3rem;
        height: 1.3rem;
        border-radius: 50%;

        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);

        background-color: var(--color-primary);
        opacity: 0;
        transition: opacity 0.2s;
      }
    }

    /* how to target the radio button */
    &__radio-input:checked + &__radio-label > &__radio-button::after {
      opacity: 1;
    }
  }
</style>
