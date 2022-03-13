<template>
  <section class=" py-10 lg:h-56 text-gray-500">
    <nav class="flex items-center flex-wrap px-4 py-5 container mx-auto">
      <a
        href="#"
        class="
          font-medium
          hover:text-blue-800
          mb-2
          mr-auto
          text-blue-600 text-xl
          uppercase
          lg:mx-auto
        "
        >just condensors</a
      >
      <button
        class="
          hover:bg-blue-600 hover:text-white
          px-3
          py-2
          rounded
          text-blue-600
          lg:hidden
        "
        data-name="nav-toggler"
        data-pg-ia='{"l":[{"name":"NabMenuToggler","trg":"click","a":{"l":[{"t":"^nav|[data-name=nav-menu]","l":[{"t":"set","p":0,"d":0,"l":{"class.remove":"hidden"}}]},{"t":"#gt# span:nth-of-type(1)","l":[{"t":"tween","p":0,"d":0.2,"l":{"rotationZ":45,"yPercent":300}}]},{"t":"#gt# span:nth-of-type(2)","l":[{"t":"tween","p":0,"d":0.2,"l":{"autoAlpha":0}}]},{"t":"#gt# span:nth-of-type(3)","l":[{"t":"tween","p":0,"d":0.2,"l":{"rotationZ":-45,"yPercent":-300}}]}]},"pdef":"true","trev":"true"}]}'
      >
        <span class="block border-b-2 border-current my-1 w-6"></span>
        <span class="block border-b-2 border-current my-1 w-6"></span>
        <span class="block border-b-2 border-current my-1 w-6"></span>
      </button>
      <div
        class="
          flex-grow
          hidden
          space-y-2
          w-full
          lg:flex lg:items-center lg:space-x-4 lg:space-y-0
        "
        data-name="nav-menu"
      >
        <div class="flex flex-col lg:flex-row mx-auto">
          <router-link :to="navItem.path"  v-for="navItem in navItems"
            :key="navItem.name"
            class="font-light hover:text-blue-600 lg:px-4 uppercase py-2 px-0"
            >{{ navItem.name }}</router-link>
        </div>
      </div>
    </nav>
  </section>
</template>

<script setup>
    const navItems = [
        {
            name: 'Home',
            path: '/'
        },
        {
            name: 'Contact',
            path: '/contact'
        }
    ]
</script>

<style scoped>

</style>