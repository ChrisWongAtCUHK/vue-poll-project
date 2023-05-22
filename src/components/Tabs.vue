<script>
export default {
  props: {
    items: Array,
    activeItem: String
  }
}
</script>

<template>
  <div class="tabs">
    <ul>
        <li v-for="item in items" :key="item" @click="$emit('setActiveItem', item)">
          <div :class="{ active: item === activeItem }">{{item}}</div>
        </li>
    </ul>
  </div>
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

  .active {
    color: #d91b42;
    border-bottom: 2px solid #d91b42;
    padding-bottom: 8px;

  }
</style>

