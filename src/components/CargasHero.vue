<template>
  <section id="hero">
    <div class="container-fluid">
      <div class="container hero__container">
        <div class="row h-100">
          <div class="heroBackground"></div>
          <div class="col-12">
            <div class="row hero__container__center">
              <div class="col-lg-auto col-12">
                <div class="hero__content">
                  <div class="col-12">
                    <p class="hero__subtitle">
                      Segurança e Qualidade para as suas
                    </p>
                  </div>

                  <div class="col-12">
                    <h1 class="hero__title">CARGAS</h1>
                  </div>

                  <div class="col-auto d-lg-block d-none">
                    <CargasLink
                      linkTitle="Faça parte do Cargas"
                      buttonClass="--white"
                      linkPage="#"
                    />
                  </div>
                </div>
              </div>

              <div
                class="
                  col-lg-5 col-md-8 col-12
                  offset-lg-0 offset-md-2 offset-0
                "
              >
                <div class="col-12">
                  <div class="hero__form">
                    <h2 class="hero__form__title">Digite a Origem e Destino</h2>

                    <div class="col-12">
                      <CargasInput
                        labelFor="origin"
                        labelTitle="Origem"
                        inputType="text"
                        inputName="origin"
                        inputPlaceholder="Cidade de Origem"
                      />
                    </div>

                    <div class="col-12">
                      <CargasInput
                        labelFor="destination"
                        labelTitle="Destino"
                        inputType="text"
                        inputName="destination"
                        inputPlaceholder="Cidade de Destino"
                      />
                    </div>

                    <div class="row marginTop24">
                      <div class="col-md-6 col-8 offset-md-0 offset-2">
                        <div class="hero__form__seePrice">
                          <span>
                            O valor do seu frete é de:
                            <span class="hero__form__seePrice --hide">
                              R$ *****
                            </span>
                          </span>
                        </div>
                      </div>

                      <div class="col-md-6 col-12">
                        <CargasBotao
                          buttonTitle="Ver Valor"
                          buttonType="submit"
                        />
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import $ from "jquery";

import CargasBotao from "./assets/CargasBotao.vue";
import CargasInput from "./assets/CargasInput.vue";
import CargasLink from "./assets/CargasLink.vue";

export default {
  components: {
    CargasBotao,
    CargasLink,
    CargasInput
  },
  data(){
    return{
      isFixed: false
    }
  }
  ,
  mounted() {
    // Como Funciona
    var hero = document.querySelector(".hero__form");

    var heroOptions = {
      root: null,

      threshold: 0.2,

      rootMargin: "0px",
    };

    var observerhero = new IntersectionObserver(function (entries) {
      entries.forEach((entry) => {
        if (!entry.isIntersecting && entry.target === hero) {
          $(".navBackground").addClass("fixed");
          $(".hero__container").addClass("navFixed");
          this.isFixed = true
        } else {
          $(".navBackground").removeClass("fixed");
          $(".hero__container").removeClass("navFixed");
          this.isFixed = false

        }
      });
    }, heroOptions);

    if (hero) {
      observerhero.observe(hero);
    }
  },
};
</script>

<style scoped>

.heroBackground {
  background-image: url("./../assets/hero.jpeg");
  height: 95vh;
  width: 100vw;

  z-index: -1;

  background-size: 100%;
  background-repeat: no-repeat;

  position: absolute;
  top: 0;
  right: 0;
  left: 0;

  opacity: 0;
  transform: translateY(-10px);

  animation: slideDown 2s forwards;
}

.hero__subtitle {
  font-family: var(--poppins);
  font-weight: var(--medium);
  font-size: var(--px24);
  color: var(--accent-0);

  opacity: 0;
  transform: translateY(-10px);

  animation: slideDown 2s 0.2s forwards;
}

.hero__title {
  font-family: var(--rcondensed);
  font-weight: var(--bold);
  color: var(--accent-0);
  font-size: 140px;

  letter-spacing: 0.015rem;

  text-shadow: -2px 4px 12px rgba(0, 0, 0, 0.5);

  opacity: 0;
  transform: translateY(-10px);

  animation: slideDown 2s forwards;
}

.hero__form {
  padding: var(--px40) var(--px32);
  background: var(--accent-0);

  opacity: 0;
  transform: translateY(-10px);

  animation: slideDown 2s forwards;
}

.hero__form__title {
  font-family: var(--rcondensed);
  font-size: var(--px32);
  font-weight: var(--bold);
  color: var(--accent-9);

  margin-bottom: var(--px24);
}

.hero__form__seePrice {
  font-size: var(--px18);
  color: var(--accent-8);

  display: inline-flex;
  align-items: center;
  height: 100%;
}

.hero__form__seePrice.--hide {
  font-size: var(--px24);
  color: var(--accent-9);
  font-weight: var(--medium);

  height: 100%;
}

.hero__form .button {
  width: 100%;
  display: block;

  font-weight: var(--bold);
  color: var(--accent-10);

  padding-top: var(--px18);
  padding-bottom: var(--px18);
}

.hero__container {
  width: auto;
  height: calc(95vh - 5rem);
}

.hero__container.navFixed {
  height: 95vh;
}

/* sm */

@media (max-width: 767.98px) {
  .hero__title {
    margin-bottom: var(--px16);
    text-align: center;
    font-size: var(--px64);
  }

  .hero__subtitle {
    font-size: var(--px16);
    text-align: center;
  }

  .heroBackground {
    background-position: top;
    background-size: auto;
  }

  .hero__form__title {
    font-size: var(--px18);
  }

  .hero__form__seePrice {
    font-size: var(--px16);
    text-align: center;
  }

  .hero__form__seePrice.--hide {
    font-size: var(--px18);
  }

  .hero__form .button {
    margin-top: var(--px24);
  }

  #hero {
    margin-bottom: 0;
  }

  .hero__content {
    margin-top: 4rem;
  }

  .hero__subtitle {
    margin-bottom: var(--px16);
  }
}

/* md */

@media (min-width: 768px) and (max-width: 1023px) {
  .hero__title {
    margin-bottom: var(--px40);
    text-align: center;
  }

  .hero__subtitle {
    text-align: center;
  }

  .heroBackground {
    background-size: auto;
  }

  #hero {
    margin-bottom: 0;
  }

  .hero__content {
    margin-top: 8rem;
  }
}

/* lg */

@media (min-width: 1024px) {
  .hero__container__center {
    display: flex;
    justify-content: space-between;

    align-items: center;

    height: 100%;
  }
}

/* full hd */

@media (min-width: 1919.98px) {
}
</style>