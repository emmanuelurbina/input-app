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
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
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
