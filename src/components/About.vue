<script setup>
import rw1 from '@/assets/rw1.jpg'
import rw3 from '@/assets/rw3.jpg'
import rw4 from '@/assets/rw4.jpg'
import rw5 from '@/assets/rw5.jpg'

const heroStyle = {
  backgroundImage: `linear-gradient(rgba(5, 34, 20, 0.58), rgba(5, 34, 20, 0.58)), url(${rw4})`,
}

const experiences = [
  {
    title: 'Local knowledge',
    image: rw1,
    text: 'We connect visitors with places, stories, and experiences that reflect Rwanda beyond the usual travel checklist.',
  },
  {
    title: 'Responsible travel',
    image: rw3,
    text: 'Our plans encourage respectful exploration, community support, and care for the natural beauty that makes Rwanda special.',
  },
  {
    title: 'Memorable journeys',
    image: rw5,
    text: 'From Kigali city walks to national parks and lakeside escapes, we shape trips that feel smooth, personal, and meaningful.',
  },
]
</script>

<template>
  <main class="bg-white text-[#163224]">
    <section
      class="relative flex min-h-[calc(100vh-72px)] items-center bg-cover bg-center px-5 py-16 text-white"
      :style="heroStyle"
      aria-labelledby="about-title"
    >
      <div class="mx-auto w-full max-w-[1180px]">
        <p class="mb-3 text-sm font-extrabold tracking-[0.12em] text-[#fff21d] uppercase">
          About Tembera Urwanda
        </p>
        <h1
          id="about-title"
          class="max-w-[820px] text-4xl leading-[1.08] font-extrabold tracking-normal drop-shadow-lg md:text-6xl lg:text-7xl"
        >
          Discover Rwanda with people who know it, love it, and share it with care.
        </h1>
        <p class="mt-6 max-w-[680px] text-lg leading-8 text-white md:text-xl">
          Tembera Urwanda helps travelers explore Rwanda through culture, nature, history, and local
          experiences. We make it easier to choose destinations, plan meaningful visits, and enjoy the
          country with confidence.
        </p>
      </div>
    </section>

    <section class="mx-auto grid max-w-[1180px] grid-cols-1 gap-11 px-[18px] pt-14 pb-8 md:px-6 lg:grid-cols-[minmax(240px,0.75fr)_minmax(0,1fr)]">
      <div>
        <p class="mb-3 text-sm font-extrabold tracking-[0.12em] text-[#d49b09] uppercase">
          Our Mission
        </p>
        <h2 class="text-3xl leading-[1.08] font-extrabold tracking-normal text-[#075f33] md:text-4xl">
          Promoting local tourism and unforgettable discovery.
        </h2>
      </div>
      <p class="m-0 text-[1.04rem] leading-8 text-[#425466]">
        Our project is built to inspire people to travel Rwanda, learn from its communities, and
        experience the beauty found in every province. Whether someone is planning a short visit or a
        longer journey, we guide them toward places worth remembering.
      </p>
    </section>

    <section class="mx-auto grid max-w-[1180px] grid-cols-1 gap-5 px-[18px] pt-6 pb-14 md:px-6 lg:grid-cols-3" aria-label="What guides us">
      <article
        v-for="experience in experiences"
        :key="experience.title"
        class="overflow-hidden rounded-lg border border-[#dbeee2] bg-[#f7fbf8]"
      >
        <img
          class="h-56 w-full object-cover"
          :src="experience.image"
          :alt="experience.title"
        >
        <div class="p-5 md:p-7">
          <h3 class="mb-3 text-xl font-extrabold text-[#087f3e]">{{ experience.title }}</h3>
          <p class="m-0 text-[1.04rem] leading-8 text-[#425466]">
            {{ experience.text }}
          </p>
        </div>
      </article>
    </section>

    <section class="mx-auto mb-12 grid max-w-[1180px] grid-cols-1 items-stretch gap-8 px-[18px] md:px-6 lg:mb-18 lg:grid-cols-[minmax(0,1fr)_360px]">
      <div class="rounded-lg bg-[#079c4a] p-5 text-white md:p-9">
        <p class="mb-3 text-sm font-extrabold tracking-[0.12em] text-white uppercase">
          Why We Exist
        </p>
        <h2 class="text-3xl leading-[1.08] font-extrabold tracking-normal text-white md:text-4xl">
          Rwanda is small on the map, but rich in experiences.
        </h2>
        <p class="mt-5 max-w-[760px] text-[1.04rem] leading-8 text-white">
          We believe travel should help people see more clearly: the landscapes, the culture, the
          creativity, and the everyday hospitality that define Rwanda. Tembera Urwanda brings those
          experiences closer to visitors and local explorers.
        </p>
      </div>

      <ul class="m-0 flex list-none flex-col justify-center gap-4 rounded-lg border border-[#f4df8e] bg-[#fff8dc] p-5 md:p-7">
        <li class="grid grid-cols-[14px_1fr] items-start gap-3 text-base leading-6 font-bold text-[#324152]">
          <span class="mt-[7px] h-2.5 w-2.5 rounded-full bg-[#079c4a]" aria-hidden="true"></span>
          Destination guidance across Rwanda
        </li>
        <li class="grid grid-cols-[14px_1fr] items-start gap-3 text-base leading-6 font-bold text-[#324152]">
          <span class="mt-[7px] h-2.5 w-2.5 rounded-full bg-[#079c4a]" aria-hidden="true"></span>
          Culture, nature, and adventure experiences
        </li>
        <li class="grid grid-cols-[14px_1fr] items-start gap-3 text-base leading-6 font-bold text-[#324152]">
          <span class="mt-[7px] h-2.5 w-2.5 rounded-full bg-[#079c4a]" aria-hidden="true"></span>
          Helpful support before and during each trip
        </li>
      </ul>
    </section>
  </main>
</template>
