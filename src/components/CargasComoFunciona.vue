<template>
    <section id="howWorks">
        <div class="container">
            <div class="col-12">
                    <h2 class="howWorks__title">
                        Como Funciona
                    </h2>
                </div>
                

                <div class="row offset-lg-3 offset-md-0 offset-1">
                    <div class="col-lg-8 col-md-12 col-11 marginBottom32 howWorks__group">
                        <div class="row">
                            <div class="howWorks__sidePath">
                                <div class="howWorks__sidePath__head">

                                </div>
                            </div>
                            <div class="col-md-6 col-12">
                                <img src="./../assets/origem-e-destino1.svg" alt="" class="svg">
                            </div>
                            <div class="col-md-6 col-12">
                                <div class="col-12">
                                    <h3 class="howWorks__subtitle">
                                        Origem e Destino
                                    </h3>
                                </div>
                                <div class="col-12">
                                    <p class="howWorks__text">
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque nec gravida quam, vitae placerat turpis. Vivamus tempor, ante in lacinia eleifend, ligula urna blandit ante, quis malesuada odio arcu in nisl. 
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-8 col-md-12 col-11 marginBottom32 howWorks__group howWorks__group--2 --desactivated">
                        <div class="row howWorks__group">
                            <div class="howWorks__sidePath">
                                <div class="howWorks__sidePath__head">

                                </div>
                            </div>

                            <div class="col-md-6 col-12 d-md-none d-block">
                                <img src="./../assets/origem-e-destino2.svg" alt="" class="svg">
                            </div>

                            <div class="col-md-6 col-12">
                                <div class="col-12">
                                    <h3 class="howWorks__subtitle">
                                        Informe os dados da sua carga
                                    </h3>
                                </div>
                                <div class="col-12">
                                    <p class="howWorks__text">
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque nec gravida quam, vitae placerat turpis. Vivamus tempor, ante in lacinia eleifend, ligula urna blandit ante, quis malesuada odio arcu in nisl. 
                                    </p>
                                </div>
                            </div>

                            <div class="col-md-6 col-12 d-md-block d-none">
                                <img src="./../assets/origem-e-destino2.svg" alt="" class="svg">
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-8 col-md-12 col-11 howWorks__group --desactivated">
                        <div class="row howWorks__group">
                            <div class="howWorks__sidePath">
                                <div class="howWorks__sidePath__head">

                                </div>
                            </div>
                            <div class="col-md-6 col-12">
                            <img src="./../assets/origem-e-destino3.svg" alt="" class="svg">
                            </div>
                            <div class="col-md-6 col-12">
                                <div class="col-12">
                                    <h3 class="howWorks__subtitle">
                                        Veja os melhores preços
                                    </h3>
                                </div>
                                <div class="col-12">
                                    <p class="howWorks__text">
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque nec gravida quam, vitae placerat turpis. Vivamus tempor, ante in lacinia eleifend, ligula urna blandit ante, quis malesuada odio arcu in nisl. 
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
import * as IO from '../js/intersectionObserver.vue'

export default {
    data() {
      return{
          IO
      }   
    }
}
</script>

<style scoped>

    #howWorks{
        padding-top: var(--px80);
        padding-bottom: var(--px80);
    }

    .howWorks__title{
        font-size: var(--px32);
        color: var(--accent-9);

        font-weight: var(--bold);

        text-align: center;

        margin-bottom: var(--px48);
    }
    
    .howWorks__subtitle{
        font-size: var(--px24);
        color: var(--accent-9);

        margin-bottom: var(--px16);

        text-transform: uppercase;
    }

    .howWorks__text{
        font-family: var(--roboto);
        font-size: var(--px18);
        color: var(--accent-7);
    }

    .howWorks__group{
        position: relative;
    }

    .howWorks__sidePath{
        position: absolute;

        top: 0;
        bottom: -32px;
        left: -16px;

        width: 4px; 
        background: var(--accent-base);

        padding: 0;
    }

    .howWorks__sidePath__head{
        position: absolute;

        top: 0;
        left: -6px;

        width: 16px;
        height: 16px;

        border-radius:100%;

        background: var(--accent-base);
    }

    .howWorks__group.--desactivated .howWorks__sidePath{
        background: var(--accent-2);
    }

    .howWorks__group.--desactivated .howWorks__sidePath__head{
        background: var(--accent-2);
    }

    .howWorks__group.--desactivated .howWorks__subtitle, .howWorks__group.--desactivated .howWorks__text, .howWorks__group.--desactivated .svg{
        opacity: 0.2;
    }

    #howWorks .svg{
        margin-bottom: var(--px8);
    }

    /* sm */

    @media (max-width: 767.98px) {



    }
    /* md */

    @media (min-width: 768px) and (max-width: 1023px) {

        
    }

    /* lg */

    @media (min-width: 1024px) and (max-width:1239.88px) {
        
    }

</style>