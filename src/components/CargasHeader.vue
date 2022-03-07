<template>
  <header>
    <nav class="navbar__top">
      <div class="container-fluid navBackground">
        <div class="container">
          <div class="row d-flex justify-content-between">
            <div class="col-lg-auto col-12">
              <a
                href="#"
                class="
                  d-flex
                  justify-content-center
                  d-lg-block
                  justify-lg-content-start
                "
              >
                <CargasLogoBase 
                
                v-if="!CargasHero.isFixed" key="navbar"

                />
                <CargasLogoPreto 
                
                v-else

                key="navbarFixed" />
              </a>
            </div>

            <div class="col-lg-auto col-12">
              <ul class="navbar__ul__links d-flex justify-content-evenly">
                <li>
                  <a href="#" class="navbar__link">
                    <div class="col-12 navbar__link__icon">
                      
                    </div>
                    <span>Inicio</span>
                  </a>
                </li>
                <li>
                  <a href="#" class="navbar__link">
                    <div class="col-12 navbar__link__icon">
                      
                    </div>
                    <span>Como Funciona</span>
                  </a>
                </li>
                <li>
                  <a href="#" class="navbar__link">
                    <div class="col-12 navbar__link__icon">
                      
                    </div>
                    <span>Cotação</span>
                  </a>
                </li>
                <li>
                  <a href="#" class="navbar__link">
                    <div class="col-12 navbar__link__icon">
                      
                    </div>
                    <span>Rastreio</span>
                  </a>
                </li>
                <li class="d-lg-flex d-none">
                  <a href="#" class="navbar__link">
                    <div class="col-12 navbar__link__icon">
                      
                    </div>
                    <span>Cadastrar-se</span>
                  </a>
                </li>
                <li>
                  <a href="#" class="navbar__link">
                    <div class="col-12 navbar__link__icon">
                      
                    </div>
                    <span>Entrar</span>
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>

  import CargasLogoBase from "./assets/CargasLogoBase.vue";
  import CargasLogoPreto from "./assets/CargasLogoPreto.vue";
  import CargasHero from ".assets/CargasHero.vue"

export default {
  components: {
    CargasLogoBase,
    CargasLogoPreto,
    CargasHero
  }
}

</script>

<style scoped>
.navbar__top {
  z-index: 9999;

}

.navBackground.fixed {
  position: fixed;

  background: var(--accent-base);

  z-index: 10000;
}

.navBackground.fixed .navbar__link span {
  color: var(--accent-9);
}

.logo {
  width: auto;
  height: 80px;

  object-fit: contain;

  padding-top: var(--px8);
  padding-bottom: var(--px8);
}

.navbar__ul__links {
  display: flex;
  align-items: center;

  height: 100%;

  z-index: 100;
}

.navbar__ul__links li {
  margin-right: var(--px16);
  margin-left: var(--px16);
}

.navbar__ul__links li:last-of-type {
  margin-right: 0;
}

.navbar__link span {
  color: var(--accent-0);

  font-family: var(--rcondensed);
  font-size: var(--px18);
  line-height: 21px;

  margin-right: 0;

  position: relative;

  transition: all 0.2s;
  -webkit-transition: all 0.2s;
  -moz-transition: all 0.2s;
  -o-transition: all 0.2s;
}

.navbar__link span::before {
  content: "";
  border-bottom: 3px solid var(--accent-9);
  position: absolute;
  left: 0;
  right: 0;
  bottom: -4px;

  width: 0%;

  transition: all 0.2s;
  -webkit-transition: all 0.2s;
  -moz-transition: all 0.2s;
  -o-transition: all 0.2s;
}

.navbar__link:hover span::before {
  width: 100%;
}

.navbar__link:hover span {
  color: var(--accent-2);
}

.navBackground.fixed .navbar__link {
  color: var(--accent-9);
}

.navbar__link__icon {
  display: none;
}

/* sm */

@media (max-width: 767.98px) {
  .navbar__ul__links {
    position: fixed;

    bottom: 0;
    right: 0;
    left: 0;

    height: auto;

    background-color: var(--accent-0);

    padding-top: var(--px8);
    padding-bottom: var(--px8);
  }

  .navbar__link span {
    font-size: var(--px10);
    color: var(--accent-9);
  }

  .navbar__ul__links li {
    margin-right: var(--px8);
    margin-left: var(--px8);
  }

  .navbar__ul__links li:last-of-type {
    margin-left: var(--px8);
    margin-right: var(--px8);
  }

  .navbar__link__icon {
    display: flex;
    justify-content: center;
  }
}

/* md */

@media (min-width: 768px) and (max-width: 1023px) {
  .navbar__ul__links {
    position: fixed;

    bottom: 0;
    right: 0;
    left: 0;

    height: auto;

    background-color: var(--accent-0);

    padding-top: var(--px16);
    padding-bottom: var(--px16);
  }

  .navbar__link span {
    font-size: var(--px16);
    color: var(--accent-9);
  }

  .navbar__ul__links li:last-of-type {
    margin-left: var(--px16);
    margin-right: var(--px16);
  }

  .navbar__link__icon {
    display: flex;
    justify-content: center;

    margin-bottom: var(--px8);
  }
}

/* lg */

@media (min-width: 1024px) {
  .navBackground.fixed {
    position: fixed;

    background: var(--accent-base);

    z-index: 10000;

    transform: translateY(-30px);

    animation: slideDown 0.2s forwards;
  }
}
</style>