<template>
  <div class="app-container">
    <app-header></app-header>
    <router-view/>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  import Component from 'vue-class-component'
  import { Header } from '@/components'

  @Component({
    components: {
      'app-header': Header,
    }
  })
  class GithubApp extends Vue {}

  export default GithubApp
</script>

<style lang="scss">
  :root {
    --primary-color: #59f;
    --bg-color: white;
    --title-color: #333;
    --text-color: #666;
    --placeholder-color: #d2cfcf;
    --disabled-color: #e5e5e5;
    --border-color: #ECE9E9;
  }

  html, body {
    font-size: 14px;
    color: var(--text-color);
    background-color: var(--bg-color);
    min-height: 100vh;
    margin: 0;
    padding: 0;
  }

  ul {
    margin: 0;
    padding: 0;
  }

  li {
    list-style: none;
  }

  a {
    color: inherit;
    text-decoration: none;
  }

  a:hover {
    color: var(--primary-color);
    text-decoration: underline;
  }

  div, section, span {
    box-sizing: border-box;
  }
</style>
