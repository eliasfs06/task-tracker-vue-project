<template>
    <header>
        <h1>
            <img src="../assets/logo.png" alt="">
        </h1>
        <button class="button" @click="darkMode">Dark mode</button>
    </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'SideBar',
    emits: ['changeTema'],
    data () {
      return {
        isDarkModeOn: false
      }
    },
    methods: {
      darkMode () {
        this.isDarkModeOn = !this.isDarkModeOn
        this.$emit('changeTema', this.isDarkModeOn)
      }
    }
})
</script>

<style>
header {
  padding: 1rem;
  background: #91c2b2;
  width: 100%;
  height: 100vh;
  text-align: center;
}
@media only screen and (max-width: 768px) {
  header {
    padding: 2.5rem;
    height: auto;
  }
}
</style>

