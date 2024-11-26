<template>
  <section class="p-4 bg-white shadow rounded-md">
    <h2 class="text-xl font-semibold mb-2">Contact Info</h2>
    <v-list class="text-gray-600">
      <v-list-item v-for="item in contactInfo" :key="item.icon" class="leading-3">   
        <template v-slot:prepend>
          <i :class="item.icon" class="rounded-full p-1 border text-gray-600 mr-2"></i>
        </template>
        <v-list-item-title class="text-gray-600">
          <a :href="item.link" target="_blank">{{ item.text }}</a>
        </v-list-item-title>
      </v-list-item>  
    </v-list>
  </section>
</template>

<script>
  export default {
    data: () => ({
      contactInfo: [
        { icon: 'fa-solid fa-location-arrow', text: 'San Miguel de Tucumán, 4000 Argentina', link: 'https://www.google.com/maps/search/?api=1&query=San+Miguel+de+Tucum%C3%A1n,+4000+Argentina' },
        { icon: 'fa-solid fa-phone', text: '+54 9 381 401-3282', link: 'tel:+5493814013282' },
        { icon: 'fa-solid fa-envelope', text: 'max.bernasconi86@gmail.com', link: 'mailto:max.bernasconi86@gmail.com' },
        { icon: 'fa-brands fa-linkedin', text: 'Max Bernasconi', link: 'https://www.linkedin.com/in/max-bernasconi-7055a9196/' },
      ],
    }),
  }
</script>
