<script>
import { ref } from 'vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import CreatePollForm from './components/CreatePollForm.vue';
import Tabs from './components/Tabs.vue'

export default {
  components: {
    Header: Header,
    Footer: Footer,
    CreatePollForm: CreatePollForm,
    Tabs: Tabs
  },
  setup() {
    const itemList = ['Current Polls', 'Add New Poll'];
    const items = ref(itemList)
    const activeItem = ref(itemList[0]);
    return {
      items, activeItem
    }
  }
}
</script>

<template>
  <Header />
  <Tabs :items="items" :activeItem="activeItem" @setActiveItem="(item) => { activeItem = item}" />
  <p v-if="activeItem === items[0]">
    Poll list component goes here
  </p>
  <p v-if="activeItem === items[1]">
    <CreatePollForm />
  </p>
  <Footer />
</template>

<style scoped>
</style>
