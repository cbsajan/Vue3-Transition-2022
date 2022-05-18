<template>
  <app-header></app-header>
  <div class="container">
    <compTransitionsThree></compTransitionsThree>
  </div>
  <app-footer></app-footer>
</template>

<script>
//import compTransitionsOne from './components/Transitions/One-Comp.vue';
//import compTransitionsTwo from './components/Transitions/Two-Comp.vue';
import compTransitionsThree from './components/Transitions/Three-Comp.vue';
export default {
  components: {
    compTransitionsThree
    // compTransitionsTwo
  }
}
</script>