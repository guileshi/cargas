<template>
  <CargasHeader />
  <CargasHero />
  <CargasComoFunciona />
  <CargasQuemSomos />
  <CargasFooter />
</template>

<script>
import CargasHeader from "./components/CargasHeader.vue";
import CargasHero from "./components/CargasHero.vue";
import CargasComoFunciona from "./components/CargasComoFunciona.vue";
import CargasQuemSomos from "./components/CargasQuemSomos.vue";
import CargasFooter from "./components/CargasFooter.vue";

export default {
  name: "App",
  components: {
    CargasHero,
    CargasHeader,
    CargasComoFunciona,
    CargasQuemSomos,
    CargasFooter
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Roboto+Condensed:ital,wght@0,300;0,400;0,700;1,700&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,300;1,400;1,500&display=swap");

:root {
  /* color */
  --accent-baseDark: #b38f00;
  --accent-base: #ffcc00;
  --accent-baseHSL: hsl(48, 100%, 50%);
  --accent-baseLight: #ffd119;
  --accent-10: #000;
  --accent-9: #121317;
  --accent-8: #3f3f42;
  --accent-7: #484848;
  --accent-6: #5b5b5b;
  --accent-5: #6f6f6f;
  --accent-4: #c7c7c7;
  --accent-3: #dbdbdb;
  --accent-2: #ebebeb;
  --accent-1: #f8f8f8;
  --accent-0: #fff;
  --accent-red: hsl(0, 81%, 38%);
  --accent-darkRed: hsl(0, 81%, 33%);
  --accent-lightRed: hsl(0, 81%, 42%);

  /* typeface weight's */
  --extrabold: 800;
  --bold: 700;
  --semibold: 600;
  --medium: 500;
  --regular: 400;
  --light: 300;

  /* typefaces */
  --roboto: "Roboto", sans-serif;
  --rcondensed: "Roboto Condensed", sans-serif;
  --poppins: "Poppins", sans-serif;

  /* pixels to rem */
  --px80: 5rem;
  --px64: 4rem;
  --px48: 3rem;
  --px40: 2.5rem;
  --px36: 2.25em;
  --px32: 2rem;
  --px24: 1.5rem;
  --px20: 1.25rem;
  --px18: 1.125rem;
  --px16: 1rem;
  --px12: 0.75rem;
  --px10: 0.65rem;
  --px8: 0.5rem;
}

* {
  margin: 0;
  padding: 0;

  font-family: var(--roboto);
  font-weight: var(--regular);
  color: var(--accent-9);
}

h2,
h3,
h4,
h5,
h6 {
  font-family: var(--rcondensed);
  color: var(--accent-9);
}

/* Chrome, Safari, Edge, Opera */
/* Remover as setas do input de numero */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type="number"] {
  -moz-appearance: textfield;
}

ul {
  margin: 0;
  padding: 0;
  align-items: center;
}

li {
  list-style: none;
}

a {
  text-decoration: none;
}

p {
  margin: 0;
}

input,
button {
  border: none;
  outline: none;
}

input {
  width: 100%;

  background-color: var(--accent-0);
  border: 1px solid var(--accent-9);

  padding: var(--px12) var(--px16);

  border-radius: 2px;

  font-size: var(--px18);
}

input:focus-visible {
  background-color: var(--accent-2);
}

.input__field {
  margin-bottom: var(--px16);
}

.input__label {
  font-size: var(--px18);
  color: var(--accent-9);

  margin-bottom: var(--px8);
}

label {
  width: 100%;
}

.button {
  padding: var(--px12) var(--px16);
  display: inline-flex;

  background: var(--accent-base);
  color: var(--accent-9);

  text-transform: uppercase;

  box-shadow: 1px 1px var(--accent-9);

  transition: all 0.2s;
  -webkit-transition: all 0.2s;
  -moz-transition: all 0.2s;
  -o-transition: all 0.2s;
}

.button:hover,
.button:focus-visible {
  transform: translate(-3px, -3px);
  box-shadow: 3px 3px var(--accent-9);
}

.button:active {
  transform: translate(0px, 0px);
  box-shadow: 0.5px 0.5px var(--accent-9);
}

.button.--white {
  background: transparent;
  color: var(--accent-0);
  font-weight: var(--bold);

  padding: var(--px12) var(--px16);
  display: inline-flex;

  border: 1px solid var(--accent-0);

  transition: all 0.2s;
  -webkit-transition: all 0.2s;
  -moz-transition: all 0.2s;
  -o-transition: all 0.2s;

  opacity: 0;

  animation: opacityFull 2s forwards;
}

.button.--white:hover {
  color: var(--accent-2);
  border: 1px solid var(--accent-2);
}

.button.--black {
  background: transparent;
  color: var(--accent-9);
  font-weight: var(--bold);

  padding: var(--px12) var(--px16);
  display: inline-flex;

  border: 1px solid var(--accent-9);

  transition: all 0.2s;
  -webkit-transition: all 0.2s;
  -moz-transition: all 0.2s;
  -o-transition: all 0.2s;

  margin-top: var(--px24);
}

.button.--black:hover {
  color: var(--accent-7);
  border: 1px solid var(--accent-7);
}

.marginTop24 {
  margin-top: var(--px24);
}

.marginBottom32 {
  margin-bottom: var(--px32);
}

.svg {
  width: 100%;
  height: auto;
  object-fit: contain;
}

@keyframes slideDown {
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes opacityFull {
  100% {
    opacity: 1;
  }
}

/* sm */

@media (max-width: 767.98px) {
  .input__label {
    font-size: var(--px16);
  }

  input {
    font-size: var(--px16);
  }

  .button.--black {
    display: block;
    text-align: center;
    width: 100%;
  }
}

/* md */

@media (min-width: 768px) and (max-width: 1023px) {
}

/* lg */

@media (min-width: 1024px) and (max-width: 1239.88px) {
}
</style>
