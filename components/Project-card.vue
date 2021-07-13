<template>
  <v-col md="4">
      <v-card
  elevation="5"
  max-width="400"
  class="mx-auto"
>
<v-img
      class="white--text align-end"
      height="200px"
      :src="`img/${card.image}`"
    >
    <v-card-title>{{card.title}}</v-card-title>
    </v-img>


<v-card-subtitle>{{card.subtitle}}</v-card-subtitle>

<v-card-actions>

      <nuxt-link :to="`/${card.id}`">
        <v-btn
        color="deep-purple lighten-2"
        text
        
      >
        View more
      </v-btn>
  
      </nuxt-link>
      
      <v-btn
        color="deep-purple lighten-2"
        text
      >
        Share
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati minus voluptates quam molestiae in optio nulla tenetur tempora, quisquam iste itaque, non doloremque necessitatibus sapiente id autem est ea labore.
        </v-card-text>
      </div>
    </v-expand-transition>
</v-card>
  </v-col>
</template>

<script>
  export default {
    props: ['card'],
    data: () => ({
      show: false,
    }),
  }
</script>

<style scoped>
nuxt-link{
  text-decoration: none;
}
</style>