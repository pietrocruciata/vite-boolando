<script>
import NavBar from './components/NavBar.vue'
import MainSection from './components/MainSection.vue'
import FooterSection from './components/FooterSection.vue'
import store from './store.js'
import axios from 'axios'


export default {
  components: {
    NavBar,
    MainSection,
    FooterSection
  },
  data: function () {
    return {
      store,
    }
  },
  mounted() {
    axios.get('http://localhost:3000/products').then((res) => {
      const data = res.data
      this.store.data = data
    })
  }

}
</script>

<template>

  <NavBar />
  <MainSection />
  <FooterSection />
</template>

<style scoped></style>
