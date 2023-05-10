<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
</script>

<template>
  <header>
    <div>
      <nav>
        <NavBar/>
        <RouterLink to="/debit">Debit Card</RouterLink>
        <RouterLink to="/credit">Credit Card</RouterLink>
        <RouterLink to="/loans">Loans</RouterLink>
        <RouterLink to="/deposit">Deposit</RouterLink>
        <RouterLink to="/sim-card">Sim-Card</RouterLink>
        <RouterLink to="/login">Login</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style lang="scss">
nav {
  display: flex;
  justify-content: space-between;
}
</style>
