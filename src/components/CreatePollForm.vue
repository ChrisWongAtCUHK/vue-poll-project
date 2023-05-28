<script>
import { ref } from 'vue'
export default {
  setup() {
    const fields = ref({question: '', answerA: '', answerB: ''})

    return {
      fields
    }
  }
}
</script>

<template>
  <form>
    <div class="form-field">
      <label for="question">Poll Question:</label>
      <input type="text" id="question" v-model="fields.question">
    </div>
    <div class="form-field">
      <label for="answer-a">Answer A:</label>
      <input type="text" id="answer-a" v-model="fields.answerA">
    </div>
    <div class="form-field">
      <label for="answer-b">Answer B:</label>
      <input type="text" id="answer-b" v-model="fields.answerB">
    </div>
  </form>
  <button @click="console.log(fields)">Add Poll</button>
</template>

<style>
input, button, select, textarea {
	font-family: inherit;
	font-size: inherit;
	-webkit-padding: 0.4em 0;
	padding: 0.4em;
	margin: 0 0 0.5em 0;
	box-sizing: border-box;
	border: 1px solid #ccc;
	border-radius: 2px;
}
</style>