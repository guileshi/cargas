<template>
  <footer class="rodape">
    <div class="container-fluid footer__background">
      <div class="container">
        <div class="row">
          <div class="col-md-4 col-12">
            <div class="row footer__group">
              <div class="col-12"><h2 class="footer__title">CARGAS</h2></div>
              <div class="col-12">
                <p class="footer__description">
                  Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                  Quam, ducimus corporis libero earum ullam explicabo autem,
                  aliquid perferendis place.
                </p>
              </div>
            </div>
          </div>
          <div class="col-lg-2 col-md-3 col-12 offset-md-1 offset-0">
            <div class="row footer__group">
              <div class="col-12">
                <h3 class="footer__list__title">Links</h3>
              </div>
              <ul class="col-12 footer__list">
                <li class="footer__link">
                  <a href="#"> Solicitar Cotação </a>
                </li>
                <li class="footer__link">
                  <a href="#"> Rastreio </a>
                </li>
                <li class="footer__link">
                  <a href="#"> Cadastrar-se </a>
                </li>
                <li class="footer__link">
                  <a href="#"> Rotas </a>
                </li>
              </ul>
            </div>
          </div>
          <div class="col-lg-2 col-md-3 offset-md-1 offset-0">
            <div class="row footer__group">
              <div class="col-12">
                <h3 class="footer__list__title">redes sociais</h3>
              </div>
              <ul class="footer__social__list">
                <li class="footer__link">
                  <a href="#"> </a>
                </li>
                <li class="footer__link"><a href="#"></a></li>
                <li class="footer__link"><a href="#"> </a></li>
              </ul>
            </div>
          </div>
        </div>
        <hr class="divider" />
        <p class="footer__copyright">
          Copyright © Todos os direitos reservados ®
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
.footer__background {
  background: var(--accent-1);

  padding-top: var(--px80);
  padding-bottom: var(--px16);
}

.footer__title {
  font-size: var(--px48);
  font-family: var(--rcondensed);
  color: var(--accent-9);

  margin-bottom: var(--px32);
  text-transform: uppercase;
}

.footer__description {
  font-size: var(--px18);
  color: var(--accent-7);

  text-align: justify;
}

.footer__list__title {
  font-size: var(--px24);
  font-family: var(--rcondensed);
  color: var(--accent-9);

  text-transform: uppercase;

  margin-bottom: var(--px16);
}

.footer__link {
  margin-bottom: var(--px8);
}

.footer__link a {
  font-size: var(--px18);
  color: var(--accent-7);
  padding-left: 4px;
}

.footer__link a:hover {
  color: var(--accent-5);
  text-decoration: underline;
}

.footer__link:last-of-type {
  margin-bottom: unset;
}

.divider {
  height: 2px;
  background-color: var(--accent-2) !important;
  opacity: 1;

  margin-top: var(--px64);
  margin-bottom: var(--px16);
}

.footer__copyright {
  font-size: var(--px18);
  color: var(--accent-7);
  text-align: center;
  font-weight: var(--medium);
}

@media (max-width: 767.98px) {
  .footer__background{
    padding-top: var(--px40);
  }
  .footer__title{
    font-size: var(--px32);
    margin-bottom: var(--px16);
  }

  .footer__description{
    font-size: var(--px16);
  }

  .footer__group:last-of-type{
    margin-bottom: var(--px32);
  }

  .divider{
    margin-top: 0;
  }

  .footer__copyright{
    font-size: var(--px16);
  }

}

@media (max-width: 1023px) {
  .footer__copyright {
    margin-bottom: 4rem;
  }
}
</style>