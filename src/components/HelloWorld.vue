

<template>
  <v-app id="inspire">
      <v-card>
        <v-layout>
      <!-- <v-system-bar color="deep-purple darken-3"></v-system-bar> -->

      <v-app-bar
        color="light"
        prominent
      >
        <!-- <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer"></v-app-bar-nav-icon> -->

        <v-toolbar-title>NavBar</v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn variant="text" >Home</v-btn>

        <v-btn variant="text" >About Us</v-btn>

        <v-btn variant="text">Contact US</v-btn>
      </v-app-bar>
      <v-main>
      
      </v-main>
    </v-layout>
      </v-card>

 <v-carousel hide-delimiters>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      cover
    ></v-carousel-item>
  </v-carousel>

  <!-- footer -->
   <v-footer class="bg-light">
    <v-row justify="center" no-gutters>
      <v-btn
        v-for="link in links"
        :key="link"
        color="black"
        variant="text"
        class="mx-2"
        rounded="xl"
      >
        {{ link }}
      </v-btn>
      <v-col class="text-center mt-2" cols="12">

      </v-col>
    </v-row>
  </v-footer>
      
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
          links: [
        'Home',
        'About Us',
        'Contact Us',
      ],
      }
    },
    
  }

</script>