<script setup>
  import StartAnimation from "./components/StartAnimation.vue";
</script>

<template>
  <header>
    <nav>
      <ul>
        <li>
          <router-link to="/">Home</router-link>
        </li>
        <li>
          <router-link to="/members">About</router-link>
        </li>
      </ul>
    </nav>
  </header>
  <StartAnimation />
  <RouterView />
</template>