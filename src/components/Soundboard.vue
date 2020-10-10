<template>
  <div id="container">
    <h3>soundboard</h3>
    <i>so, uh, polibot couldn't get it together—enjoy some dings and/or dongs.</i>
    <p></p>
    <i>(:sir:)</i>
    <!-- <i>. keep an eye on the <a href="https://github.com/mattpolicastro/polibot" target="_blank" rel="noopener">github repo</a>.</i> -->
    <div class="layer" id="soundboard">
      <button @click.prevent="playSound()">hello</button>
      <button @click.prevent="playSound()">hey</button>
      <button @click.prevent="playSound()">really?</button>
      <button @click.prevent="playSound()">normality</button>
    </div>
    <!-- <div class="layer" id="maintenance"> -->

    <!-- </div> -->
  </div>

</template>

<script>
module.exports = {
  methods: {
    playSound () {
      var sounds = ['http://soundbible.com/mp3/Elevator Ding-SoundBible.com-685385892.mp3', 'http://soundbible.com/mp3/Air Plane Ding-SoundBible.com-496729130.mp3']
      var soundIndex = Math.round(Math.random());
      var audio = new Audio(sounds[soundIndex]);
      audio.play();
    }
  }
}
</script>

<style scoped>
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
}
#maintenance {
  z-index: 10;
  margin: 4em auto;
  padding: auto;
  background-color: hsla(340, 0%, 50%, 0.5);
}
</style>
