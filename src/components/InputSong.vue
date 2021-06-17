<template>
<form @submit.prevent="submitInputs">
  <label for="">Title: </label>
  <input type="text" v-model="title">
  <label for="">Artist: </label>
  <input type="text" v-model="artist">
  <label for="">Year: </label>
  <input type="text" v-model="year">
  <button>Submit</button>
</form>
<p>{{ title }}</p>
<p>{{ artist }}</p>
<p>{{ year }}</p>
</template>

<script>
export default {
  data() {
    return {
      title: '',
      artist: '',
      year: ''
    }
  },
  methods: {
    submitInputs() {
      const newSong = {
        title: this.title,
        artist: this.artist,
        year: this.year
      }
      this.$emit('addSong', newSong)
      this.title = ''
      this.artist = ''
      this.year = ''
    }
  }
}
</script>