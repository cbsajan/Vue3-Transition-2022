<template>
  <app-header></app-header>
  <div class="container">
    <compTransitionsTwo></compTransitionsTwo>
  </div>
  <app-footer></app-footer>
</template>

<script>
//import compTransitionsOne from './components/Transitions/One-Comp.vue';
import compTransitionsTwo from './components/Transitions/Two-Comp.vue';
export default {
  components: {
    compTransitionsTwo
  }
}
</script>