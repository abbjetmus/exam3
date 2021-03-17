<template>
  <v-container>
    <v-row>
      <v-col
        v-for="photo in photos"
        :key="photo.id"
      >
        <v-card
          class="mx-auto"
          max-width="344"
        >
          <v-img
            :src="photo.thumbnailUrl"
            height="200px"
          ></v-img>

          <v-card-title>
            {{photo.title}}
          </v-card-title>

          <v-card-subtitle>
            {{photo.url}}
          </v-card-subtitle>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',
  created () {
    fetch('https://jsonplaceholder.typicode.com/photos')
      .then(response => response.json())
      .then(json => {
        this.photos = json.slice(0, 10)
      })
  },
  data () {
    return {
      photos: []
    }
  }
}
</script>
