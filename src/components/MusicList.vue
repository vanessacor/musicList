<template>
  <div>
    <h2>Ayu and Vanessa Favourite Songs</h2>
    <ul>
      <li v-for="song in musicList" :key="song.title">{{ song.title }}</li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      musicList: [
        { title: "Fisherman Blues", artist: "Waterboys", year: "1997" },
        { title: "It is My Life", artist: "Bon Jovi", year: "1999" },
      ],
    };
  },
};
</script>