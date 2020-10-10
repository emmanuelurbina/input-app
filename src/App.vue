<template>
  <div id="app">
    <input-view />
  </div>
</template>

<script>
import InputView from "./views/InputView.vue"

export default {
  name: 'App',
  components: {
    'input-view': InputView
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500&display=swap');
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Noto Sans JP', sans-serif;
  font-weight: 500;
  font-size: 14px;
}

#app {
  margin: 5em;
}

@media screen and (max-width: 600px) {
  #app {
    margin: 2em 5px;
  }
}
</style>
