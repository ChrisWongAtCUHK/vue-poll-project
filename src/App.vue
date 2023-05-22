<script>
import { ref } from 'vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  components: {
    Header: Header,
    Footer: Footer
  },
  props : {
    
  },
  setup() {
    const itemList = ['Current Polls', 'Add New Poll'];
    const items = ref(itemList)
    const activeItem = ref(itemList[0]);
    return {
      items, activeItem
    }
  },

  mounted() {
    console.log(this.items)
    console.log(this.activeItem)
  }
}
</script>

<template>
  <Header />
  <Footer />
</template>

<style scoped>
</style>
