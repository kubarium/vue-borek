<template>
<div class="letter">

  <span>
				{{letter}}
				</span>
				<div class="controller">
					<button class="material-icons">grain</button>
					<button class="material-icons">keyboard_arrow_up</button>
					<button class="material-icons">shuffle</button>
					<button class="material-icons">keyboard_arrow_left</button>
					<input type="text" value="99" class="letter-stepper" disabled>
					<button class="material-icons">keyboard_arrow_right</button>
                    <button><icon name="hand-o-left"/></button>
					<button class="material-icons">keyboard_arrow_down</button>
                    <button><icon name="hand-o-right"/></button>
					<button><icon name="check-square-o"/></button>
</div>
				</div>
</template>

<script>
export default {
  props: ["letter"]
};
</script>

<style>
.controller {
  display: grid;
  grid-template-columns: repeat(3, 21px);
  grid-template-columns: repeat(3, 21px);

  /*
    grid-template-areas:"button button button"
                        "button input button"
                        "button button button";
    */

  background-color: white;
  border-radius: 2px;
  border: 1px solid #dbdbdb;
  width: 63px;
  height: 63px;
}

.material-icons {
  font-family: "Material Icons";
  font-weight: normal;
  font-style: normal;
  font-size: 21px; /* Preferred icon size */
  display: inline-block;
  line-height: 1;
  text-transform: none;
  letter-spacing: normal;
  word-wrap: normal;
  white-space: nowrap;
  direction: ltr;

  /* Support for all WebKit browsers. */
  -webkit-font-smoothing: antialiased;
  /* Support for Safari and Chrome. */
  text-rendering: optimizeLegibility;

  /* Support for Firefox. */
  -moz-osx-font-smoothing: grayscale;

  /* Support for IE. */
  font-feature-settings: "liga";
}
.controller input {
  width: 21px;
  height: 21px;
  text-align: center;
  border: none;
  box-sizing: border-box;
  background-color: white;
  outline: 0;
}

.controller button {
  text-align: center;
  width: 21px;
  height: 21px;
  margin: 0;
  padding: 0;
  border: none;
  background: none;
}
</style>
