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
  <div class="tabs">
    <ul>
        <li v-for="item in items" :key="item">
          <div >{{item}}</div>
        </li>
    </ul>
  </div>
  <Footer />
</template>

<style scoped>
  ul {
    display: flex;
    justify-content: center;
    padding: 0;
    list-style-type: none;
  }

  li {
    margin: 0 16px;
    font-size: 18px;
    color: #555;
    cursor: pointer;
  }
  
  .tabs {
    margin-bottom: 40px;
  }
</style>
