<script setup>
import rw1 from '@/assets/rw1.jpg'
import rw3 from '@/assets/rw3.jpg'
import rw4 from '@/assets/rw4.jpg'
import rw5 from '@/assets/rw5.jpg'

const heroStyle = {
  backgroundImage: `linear-gradient(rgba(4, 35, 20, 0.54), rgba(4, 35, 20, 0.54)), url(${rw4})`,
}

const features = [
  {
    number: '01',
    title: 'Plan your trip',
    text: 'Find destinations, travel ideas, and helpful guidance before you start moving.',
  },
  {
    number: '02',
    title: 'Explore Rwanda',
    text: 'Discover culture, wildlife, lakes, hills, cities, and local experiences across the country.',
  },
  {
    number: '03',
    title: 'Travel with care',
    text: 'Choose experiences that respect communities, nature, and Rwanda’s unique heritage.',
  },
]

const destinations = [
  {
    name: 'Nature Escapes',
    image: rw1,
    text: 'Green hills, quiet views, and fresh air for travelers who love peaceful places.',
  },
  {
    name: 'Culture Trips',
    image: rw3,
    text: 'Meet stories, traditions, creativity, and daily life that make Rwanda memorable.',
  },
  {
    name: 'Adventure Days',
    image: rw5,
    text: 'Create full days around parks, lakes, city walks, and scenic journeys.',
  },
]
</script>

<template>
  <main class="bg-white text-[#163224]">
    <section
      class="relative flex min-h-[calc(100vh-72px)] items-center bg-cover bg-center px-5 py-16 text-white"
      :style="heroStyle"
      aria-labelledby="home-title"
    >
      <div class="mx-auto w-full max-w-[1180px]">
        <p class="mb-3 text-sm font-extrabold tracking-[0.14em] text-[#fff21d] uppercase">
          Visit Rwanda your way
        </p>
        <h1
          id="home-title"
          class="max-w-[850px] text-4xl leading-[1.05] font-extrabold tracking-normal drop-shadow-lg md:text-6xl lg:text-7xl"
        >
          Welcome to Tembera U Rwanda
        </h1>
        <p class="mt-6 max-w-[680px] text-lg leading-8 text-white md:text-xl">
          Explore Rwanda through beautiful destinations, local culture, nature experiences, and travel
          ideas made for unforgettable journeys.
        </p>

        <div class="mt-8 flex flex-col gap-4 sm:flex-row">
          <RouterLink
            to="/about"
            class="inline-flex items-center justify-center rounded-md bg-[#fff21d] px-6 py-3 text-base font-extrabold text-[#075f33] shadow-lg transition hover:bg-white"
          >
            Learn About Us
          </RouterLink>
          <RouterLink
            to="/services"
            class="inline-flex items-center justify-center rounded-md border border-white px-6 py-3 text-base font-extrabold text-white transition hover:bg-white hover:text-[#075f33]"
          >
            Explore Services
          </RouterLink>
        </div>
      </div>
    </section>

    <section class="mx-auto grid max-w-[1180px] grid-cols-1 gap-5 px-[18px] py-14 md:px-6 lg:grid-cols-3">
      <article
        v-for="feature in features"
        :key="feature.title"
        class="rounded-lg border border-[#dbeee2] bg-[#f7fbf8] p-6"
      >
        <p class="mb-5 text-sm font-extrabold text-[#d49b09]">{{ feature.number }}</p>
        <h2 class="mb-3 text-2xl font-extrabold text-[#087f3e]">{{ feature.title }}</h2>
        <p class="m-0 text-base leading-7 text-[#425466]">{{ feature.text }}</p>
      </article>
    </section>

    <section class="bg-[#f2faf5] py-14">
      <div class="mx-auto max-w-[1180px] px-[18px] md:px-6">
        <div class="mb-8 max-w-[720px]">
          <p class="mb-3 text-sm font-extrabold tracking-[0.12em] text-[#d49b09] uppercase">
            Featured Experiences
          </p>
          <h2 class="text-3xl leading-tight font-extrabold text-[#075f33] md:text-4xl">
            Start with the places and moments people remember most.
          </h2>
        </div>

        <div class="grid grid-cols-1 gap-5 lg:grid-cols-3">
          <article
            v-for="destination in destinations"
            :key="destination.name"
            class="overflow-hidden rounded-lg bg-white shadow-[0_16px_36px_rgba(7,95,51,0.12)]"
          >
            <img
              class="h-60 w-full object-cover"
              :src="destination.image"
              :alt="destination.name"
            >
            <div class="p-6">
              <h3 class="mb-3 text-2xl font-extrabold text-[#087f3e]">{{ destination.name }}</h3>
              <p class="m-0 text-base leading-7 text-[#425466]">{{ destination.text }}</p>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="mx-auto grid max-w-[1180px] grid-cols-1 items-center gap-8 px-[18px] py-14 md:px-6 lg:grid-cols-[1fr_0.7fr]">
      <div>
        <p class="mb-3 text-sm font-extrabold tracking-[0.12em] text-[#d49b09] uppercase">
          Ready To Go
        </p>
        <h2 class="text-3xl leading-tight font-extrabold text-[#075f33] md:text-4xl">
          Your next Rwanda experience can start here.
        </h2>
        <p class="mt-4 max-w-[680px] text-base leading-8 text-[#425466]">
          Whether you are visiting for the first time or rediscovering home, Tembera U Rwanda helps
          you find meaningful places to explore.
        </p>
      </div>

      <RouterLink
        to="/contact"
        class="inline-flex w-full items-center justify-center rounded-md bg-[#079c4a] px-6 py-4 text-base font-extrabold text-white transition hover:bg-[#087f3e] sm:w-auto lg:justify-self-end"
      >
        Contact Us
      </RouterLink>
    </section>
  </main>
</template>
