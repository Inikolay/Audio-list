<template>
  <div id="app">
    <Header />
    <DoUseIt />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import DoUseIt from './components/DoUseIt.vue'

export default {
  name: 'App',
  components: {
   Header,
   DoUseIt,
  }
}
</script>

