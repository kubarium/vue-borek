<template>
  <div id="app">
    <input type="text" id="entry" v-model="letters" />
		<div class="letters">			
				<LetterSpinner v-for="letter in letters" letter="letter" v-bind:letter="letter"/>			
		</div>
		
  </div>
</template>

<script>
import Vue from "vue";

import LetterSpinner from "./LetterSpinner.vue";
import Icon from "vue-awesome/components/Icon";

import "vue-awesome/icons";
Vue.component("icon", Icon);

export default {
  name: "app",
  data() {
    return {
      letters: "yuck"
    };
  },
  components: {
    LetterSpinner
  }
};
</script>

<style lang="scss">
.letters {
  display: grid;
  grid-template-columns: repeat(4, 98px);
  grid-gap: 10px;
}
.letter {
  width: 96px;
  height: 117px;
  background-color: #f5f5f5;
  border: 1px solid #dbdbdb;
  border-radius: 3px;
}

body {
  background-color: white;
}
</style>
