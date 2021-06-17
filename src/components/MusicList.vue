<template>
  <section>
    <h2>Ayu and Vanessa Favourite Songs</h2>
    <ul>
      <li v-for="song in musicList" :key="song.title">{{ song.title }}</li>
    </ul>
  </section>
    <InputSong @addSong="addSongToList"/>
</template>
<script>
  import InputSong from "./InputSong.vue"
export default {
  components: { InputSong },

  data() {
    return {
      musicList: [
        { title: "Fisherman Blues", artist: "Waterboys", year: "1997" },
        { title: "It is My Life", artist: "Bon Jovi", year: "1999" },
      ],
    };
  },
  methods: {
    addSongToList(song) {
      console.log(song)
      this.musicList.push(song)
    }
  }
};
</script>