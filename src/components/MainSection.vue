<script>
import CardComponents from './CardComponents.vue'
// import DataProducts from '/db.json'
import store from '../store.js';


export default {
    data() {
        return {
            store,
        }
    },
    components: {
        CardComponents,
    },

    mounted() {
        console.log(this.store.data.products);
    }

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
                        <CardComponents v-for="(product, i) in store.data" :key="product.id" :item="product" />
                    </div>
                </div>
            </div>
        </section>
    </main>


</template>

<style lang="scss" scoped>
@use './style/general'
</style>
