<script setup>
import { ref } from 'vue'

const openMenu = ref('')

function toggleMenu(menuName) {
  openMenu.value = openMenu.value === menuName ? '' : menuName
}

function showMenu(menuName) {
  openMenu.value = menuName
}

function closeMenu() {
  openMenu.value = ''
}
</script>

<template>
  <nav class="navbar">
    <img class="navbar-logo" src="/Logo.png" alt="Logo">
    <span class="navbar-brand">TEMBERURWANDA</span>
    <ul class="navbar-links">
      <li><RouterLink to="/" class="hover:text-yellow-300">Home</RouterLink></li>
      <li><RouterLink to="/about" class="hover:text-yellow-300">About us</RouterLink></li>
      <li><RouterLink to="/services" class="hover:text-yellow-300">Services</RouterLink></li>
      <li class="dropdown-item" @mouseenter="showMenu('gallery')" @mouseleave="closeMenu">
        <button
          class="navbar-button hover:text-yellow-300"
          type="button"
          :aria-expanded="openMenu === 'gallery'"
          @click="toggleMenu('gallery')"
          @focus="showMenu('gallery')"
        >
          Gallery <span class="dropdown-arrow">v</span>
        </button>

        <div v-if="openMenu === 'gallery'" class="navbar-dropdown">
          <RouterLink to="/services" @click="openMenu = ''">Videos</RouterLink>
          <RouterLink to="/services" @click="openMenu = ''">Photos</RouterLink>
        
        </div>
      </li>
      <li class="dropdown-item" @mouseenter="showMenu('destination')" @mouseleave="closeMenu">
        <button
          class="navbar-button hover:text-yellow-300"
          type="button"
          :aria-expanded="openMenu === 'destination'"
          @click="toggleMenu('destination')"
          @focus="showMenu('destination')"
        >
          Destination <span class="dropdown-arrow">v</span>
        </button>

        <div v-if="openMenu === 'destination'" class="navbar-dropdown">
          <RouterLink to="/services" @click="openMenu = ''">Eastern province</RouterLink>
          <RouterLink to="/services" @click="openMenu = ''">Western province</RouterLink>
          <RouterLink to="/services" @click="openMenu = ''">Northern province</RouterLink>
          <RouterLink to="/services" @click="openMenu = ''">Southern province</RouterLink>
          <RouterLink to="/services" @click="openMenu = ''">Kigali city</RouterLink>
        </div>
      </li>
      <li><RouterLink to="/contact" class="hover:text-yellow-300">Contact</RouterLink></li>
    </ul>
  </nav>
</template>
