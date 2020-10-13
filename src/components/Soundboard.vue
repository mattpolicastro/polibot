<template>
  <div id="container">
    <h3>soundboard</h3>
    <i>polibot is still collecting clips; in the meantime,</i>
    <br>
    <i>enjoy some dings and/or dongs.</i>
    <br>
    <i>(:sir:)</i>
    <div class="layer" id="soundboard">
      <button v-for="sound in sounds" :key="sound.pathShort" @click.prevent="playSound(sound.pathLong)">{{sound.pathShort.replace(/\.\//, '').replace(/\.mp3$/, '').replace(/_/g, ' ')}}</button>
    </div>
    <button @click.prevent="playSound('http://soundbible.com/mp3/Elevator Ding-SoundBible.com-685385892.mp3')">ding</button>
    <button @click.prevent="playSound('http://soundbible.com/mp3/Air Plane Ding-SoundBible.com-496729130.mp3')">dong</button>
  </div>

</template>

<script>

module.exports = {
  data() {
    return {
      sounds: []
    };
  },
  // The `importSounds` workaround for sound file loading inspired by: https://stackoverflow.com/questions/54095215/how-to-get-all-the-image-files-in-a-directory-using-vue-js-nuxt-js
  mounted() {
    this.importSounds(require.context('../assets/sounds', true, /\.mp3$/));
  },
  methods: {
    importSounds(r) {
      r.keys().forEach(key => (
        this.sounds.push({ pathLong: r(key), pathShort: key})
      ));
    },
    playSound (sound) {
      if (sound) {
        var audio = new Audio(sound);
        audio.play();
      }
    }
  }
}
</script>

<style scoped>
#container {
  max-width: 40em;
  margin: auto;
}
button {
  margin: 1em;
  padding: auto;
  width: 7em;
  height: 5em;
  flex: none;
  text-transform: uppercase;
  background-color: rgb(226, 247, 254);
  border: none;
  color: #32C4F5;
  outline: none !important;
  font-weight: bold;
}
button:hover {
  color: white;
  background-color: rgb(76, 204, 246);
  transition: 0.3s;
}
#soundboard {
  display: flex;
  align-items: center;
  align-content: flex-start;
  justify-content: center;
  flex-wrap: wrap;
}
#maintenance {
  z-index: 10;
  margin: 4em auto;
  padding: auto;
  background-color: hsla(340, 0%, 50%, 0.5);
}
</style>
