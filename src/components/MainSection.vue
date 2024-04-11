<script>
import CardComponents from './CardComponents.vue'
import DataProducts from '../assets/db.json'

export default {
    data() {
        return {

            product: DataProducts.products
        }
    },
    components: {
        CardComponents
    },

}


</script>

<template>

    <!--ELEMENTS SHOP-->

    <!--FIRST ELEMENT-->
    <main class="d-flex jc-center f-wrap">
        <section>
            <div class="container-central">
                <div class="row p-relative card">
                    <div class="col-1 dispositions-cards">
                        <!-- CARD 1 -->
                        <CardComponents v-for="(product, i) in product" :key="product.id" :item="product" />


                        <!-- <div class="card">
                            <div class="p-relative">
                                <img class="img-first max-w" src="/public/img/2.webp" alt="">
                                <img class="img-second max-w" src="/public/img/2b.webp" alt="">
                                <div class="badge-red bg-red">-30%</div>
                                <div class="hearts">&hearts;</div>
                            </div>
                            <figcaption>
                                <ul class="p-m-not">
                                    <li class="c-lightgrey">Guess</li>
                                    <li><strong>ROSES TEE</strong></li>
                                    <li class="c-red">20,89€€ <span class="c-black line-through">29,99€</span></li>
                                </ul>
                            </figcaption>
                        </div>
                     CARD 3 
                        <div class="card">
                            <div class="p-relative">
                                <img class="img-first max-w" src="/public/img/3.webp" alt="">
                                <img class="img-second max-w" src="/public/img/3b.webp" alt="">
                                <div class="badge-red bg-red">-30%</div>
                                <div class="hearts">&hearts;</div>
                            </div>
                            <figcaption>
                                <ul class="p-m-not">
                                    <li class="c-lightgrey">Come zucchero filato</li>
                                    <li><strong>VOGLIA DI COLORI PASTELLO</strong></li>
                                    <li class="c-red">128,99€ <span class="c-black line-through">184,99€</span></li>
                                </ul>
                            </figcaption>
                        </div>
                         CARD 4 
                        <div class="card">
                            <div class="p-relative">
                                <img class="img-first max-w" src="/public/img/4.webp" alt="">
                                <img class="img-second max-w" src="/public/img/4b.webp" alt="">
                                <div class="badge-red bg-red">-50%</div>
                                <div class="badge-green bg-green">Sostenibilità</div>
                                <div class="hearts">&hearts;</div>
                            </div>
                            <figcaption>
                                <ul class="p-m-not">
                                    <li class="c-lightgrey">levi's</li>
                                    <li><strong>TEE UNISEX</strong></li>
                                    <li class="c-red">14,99€ <span class="c-black line-through">29,99€</span></li>
                                </ul>
                            </figcaption>
                        </div>
                        CARD 5 
                        <div class="card">
                            <div class="p-relative">
                                <img class="img-first max-w" src="/public/img/5.webp" alt="">
                                <img class="img-second max-w" src="/public/img/5b.webp" alt="">
                                <div class="badge"></div>
                                <div class="hearts">&hearts;</div>
                            </div>
                            <figcaption>
                                <ul class="p-m-not">
                                    <li class="c-lightgrey">Maya Deluxe</li>
                                    <li><strong>STRIPE BODICE</strong></li>
                                    <li class="c-red">99,99€ </li>
                                </ul>
                            </figcaption>
                        </div>
                        CARD 6 
                        <div class="card">
                            <div class="p-relative">
                                <img class="img-first max-w" src="/public/img/6.webp" alt="">
                                <img class="img-second max-w" src="/public/img/6b.webp" alt="">
                                <div class="only-sos bg-green">Sostenibilità</div>
                                <div class="hearts">&hearts;</div>
                            </div>
                            <figcaption>
                                <ul class="p-m-not">
                                    <li class="c-lightgrey">Esprit</li>
                                    <li><strong>MAGLIONE-BLACK</strong></li>
                                    <li class="c-red">29,99€</li>
                                </ul>
                            </figcaption>
                        </div> -->
                    </div>
                </div>
            </div>
        </section>


    </main>


</template>

<style lang="scss" scoped>
@use './style/general'
</style>
