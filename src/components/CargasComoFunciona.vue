<template>
  <section id="howWorks">
    <div class="container">
      <div class="col-12">
        <div class="d-flex justify-content-center">
          <h2 class="howWorks__title">Como Funciona</h2>
        </div>
      </div>

      <div class="row offset-lg-3 offset-md-0 offset-1">
        <div class="col-lg-8 col-md-12 col-11 marginBottom32 howWorks__group">
          <div class="row">
            <div class="howWorks__sidePath">
              <div class="howWorks__sidePath__head"></div>
            </div>
            <div class="col-md-6 col-12">
              <img src="./../assets/origem-e-destino1.svg" alt="" class="svg" />
            </div>
            <div class="col-md-6 col-12">
              <div class="col-12">
                <h3 class="howWorks__subtitle">Origem e Destino</h3>
              </div>
              <div class="col-12">
                <p class="howWorks__text">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                  Pellentesque nec gravida quam, vitae placerat turpis. Vivamus
                  tempor, ante in lacinia eleifend, ligula urna blandit ante,
                  quis malesuada odio arcu in nisl.
                </p>
              </div>
            </div>
          </div>
        </div>

        <div
          class="
            col-lg-8 col-md-12 col-11
            marginBottom32
            howWorks__group howWorks__group--2
            --desactivated
          "
        >
          <div class="row">
            <div class="howWorks__sidePath">
              <div class="howWorks__sidePath__head"></div>
            </div>

            <div class="col-md-6 col-12 d-md-none d-block">
              <img src="./../assets/origem-e-destino2.svg" alt="" class="svg" />
            </div>

            <div class="col-md-6 col-12">
              <div class="col-12">
                <h3 class="howWorks__subtitle">
                  Informe os dados da sua carga
                </h3>
              </div>
              <div class="col-12">
                <p class="howWorks__text">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                  Pellentesque nec gravida quam, vitae placerat turpis. Vivamus
                  tempor, ante in lacinia eleifend, ligula urna blandit ante,
                  quis malesuada odio arcu in nisl.
                </p>
              </div>
            </div>

            <div class="col-md-6 col-12 d-md-block d-none">
              <img src="./../assets/origem-e-destino2.svg" alt="" class="svg" />
            </div>
          </div>
        </div>

        <div
          class="
            col-lg-8 col-md-12 col-11
            howWorks__group howWorks__group--3
            --desactivated
          "
        >
          <div class="row">
            <div class="howWorks__sidePath">
              <div class="howWorks__sidePath__head"></div>
            </div>
            <div class="col-md-6 col-12">
              <img src="./../assets/origem-e-destino3.svg" alt="" class="svg" />
            </div>
            <div class="col-md-6 col-12">
              <div class="col-12">
                <h3 class="howWorks__subtitle">Veja os melhores preços</h3>
              </div>
              <div class="col-12">
                <p class="howWorks__text">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                  Pellentesque nec gravida quam, vitae placerat turpis. Vivamus
                  tempor, ante in lacinia eleifend, ligula urna blandit ante,
                  quis malesuada odio arcu in nisl.
                </p>
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

export default {
  mounted() {
    // Como Funciona
    var howWorks = document.querySelector(".howWorks__group--2");

    var howWorksOptions = {
      root: null,

      threshold: 1,

      rootMargin: "0px",
    };

    var observerHowWorks = new IntersectionObserver(function (entries) {
      entries.forEach((entry) => {
        if (entry.isIntersecting && entry.target === howWorks) {
          $(".howWorks__group--2").removeClass("--desactivated");
          $(".howWorks__group--2").addClass("--activated");
        }
      });
    }, howWorksOptions);

    if (howWorks) {
      observerHowWorks.observe(howWorks);
    }

    // Como Funciona
    var howWorks2 = document.querySelector(".howWorks__group--3");

    var howWorksOptions2 = {
      root: null,

      threshold: 1,

      rootMargin: "0px",
    };

    var observerHowWorks2 = new IntersectionObserver(function (entries) {
      entries.forEach((entry) => {
        if (entry.isIntersecting && entry.target === howWorks2) {
          $(".howWorks__group--3").removeClass("--desactivated");
          $(".howWorks__group--3").addClass("--activated");
        }
      });
    }, howWorksOptions2);

    if (howWorks2) {
      observerHowWorks2.observe(howWorks2);
    }
  },
};
</script>

<style scoped>
#howWorks {
  padding-bottom: var(--px80);

  margin-top: var(--px80);
}

.howWorks__title {
  font-size: var(--px32);
  color: var(--accent-9);

  font-weight: var(--bold);

  margin-bottom: var(--px48);

  position: relative;

  display: flex;
  justify-content: center;
}

.howWorks__title::before {
  content: "";

  position: absolute;

  border-bottom: 6px solid var(--accent-base);
  border-radius: 4px;

  bottom: 4px;
  left: -8px;
  width: 50%;

  z-index: -1;
}

.howWorks__subtitle {
  font-size: var(--px24);
  color: var(--accent-9);

  margin-bottom: var(--px16);

  text-transform: uppercase;

  position: relative;
}

.howWorks__text {
  font-family: var(--roboto);
  font-size: var(--px18);
  color: var(--accent-7);
}

.howWorks__group {
  position: relative;
}

.howWorks__sidePath {
  position: absolute;

  top: 0;
  bottom: -32px;
  left: -16px;

  width: 4px;
  background: var(--accent-base);

  padding: 0;
}

.howWorks__sidePath__head {
  position: absolute;

  top: 0;
  left: -6px;

  width: 16px;
  height: 16px;

  border-radius: 100%;

  background: var(--accent-base);
}

.howWorks__group.--desactivated .howWorks__sidePath,
.howWorks__group.--desactivated .howWorks__sidePath__head {
  background: var(--accent-2);
}

.howWorks__group.--activated .howWorks__sidePath,
.howWorks__group.--activated .howWorks__sidePath__head {
  transition: all 2s;
  background: var(--accent-base);
}

.howWorks__group.--desactivated .howWorks__subtitle,
.howWorks__group.--desactivated .howWorks__text,
.howWorks__group.--desactivated .svg {
  opacity: 0.2;
}

.howWorks__group.--activated .howWorks__subtitle,
.howWorks__group.--activated .howWorks__text,
.howWorks__group.--activated .svg {
  opacity: 1;
  transition: all 2s;
}

#howWorks .svg {
  margin-bottom: var(--px8);
}

/* sm */

@media (max-width: 767.98px) {
  #howWorks {
    margin-top: var(--px64);
  }

  .howWorks__title {
    font-size: var(--px24);
  }

  .howWorks__text {
    font-size: var(--px16);
  }

  .howWorks__subtitle {
    font-size: var(--px18);
  }
}
/* md */

@media (min-width: 768px) and (max-width: 1023px) {

  #howWorks {
    margin-top: unset;
  }

}

/* lg */

@media (min-width: 1024px) and (max-width: 1239.88px) {
}
</style>