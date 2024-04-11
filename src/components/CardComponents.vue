<script>
export default {
    props: {
        item: {
            type: Object
        }
    },
    methods: {
        getDiscount() {

            let finalPrice = 0
            if (this.product.badges.type === 'discount' && this.product.badges.value === '-50%') {
                let rest50 = this.product.badges.price * 0.5.toFixed(2);
                finalPrice = this.product.badges.price - rest50
            } else {
                let rest30 = this.product.badges.price * 0.3.toFixed(2);
                finalPrice = this.product.badges.price - rest30
            }
            return finalPrice
        }
    }


}
</script>

<template>
    <div class="card">
        <div class="p-relative">
            <img class="img-first max-w" :src="`/img/${item.frontImage}`" alt="">
            <img class="img-second max-w" :src="`/img/${item.backImage}`" alt="">
            <div v-for="(badge, i) in item.badges" :key="i"
                :class="badge.type === 'discount' ? 'badge-red bg-red' : 'badge-green bg-green'">{{ badge.value }}</div>

            <div class="hearts">&hearts;</div>
        </div>
        <figcaption>

            <ul class="p-m-not">
                <li class="c-lightgrey">{{ item.brand }}</li>
                <li><strong>{{ item.name }}</strong></li>
                <li v-for="(discount, i) in item.badges" :key="i">
                    <div class="c-red" v-if="discount.value === '-50%' && discount.type === 'discount'">
                        <span>{{ (item.price - (item.price * 0.5)).toFixed(2) }} &euro;</span>
                        <span class="c-black line-through">{{ item.price }} &euro;</span>
                    </div>

                    <div class="c-red " v-else-if="discount.value === '-30%' && discount.type === 'discount'">
                        <span>{{ (item.price - (item.price * 0.3)).toFixed(2) }} &euro;</span>
                        <span class="c-black line-through">{{ item.price }} &euro;</span>
                    </div>
                    <div v-else-if="item.badges.length < 2 && discount.type === 'tag'">
                        <span class="c-black ">{{ item.price }} &euro;</span>
                    </div>
                </li>

            </ul>
        </figcaption>
    </div>
</template>

<style lang="scss" scoped>
@use './style/general'
</style>