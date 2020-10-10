<template>
  <div id="container">
    <h3>soundboard</h3>
    <i>polibot is still collecting files; in the meantime, enjoy some dings and/or dongs.</i>
    <p></p>
    <i>(:sir:)</i>
    <!-- <i>. keep an eye on the <a href="https://github.com/mattpolicastro/polibot" target="_blank" rel="noopener">github repo</a>.</i> -->
    <div class="layer" id="soundboard">
      <button @click.prevent="playSound(require('../assets/sounds/hello.mp3'))">hello</button>
      <button @click.prevent="playSound(require('../assets/sounds/hey.mp3'))">hey</button>
      <button @click.prevent="playSound(require('../assets/sounds/hows_it_going.mp3'))">how's it going?</button>
      <button @click.prevent="playSound(require('../assets/sounds/laugh_high.mp3'))">laugh (high)</button>
      <button @click.prevent="playSound(require('../assets/sounds/laugh_low.mp3'))">laugh (low)</button>
      <button @click.prevent="playSound(require('../assets/sounds/lemmethinkonthat.mp3'))">lemme think</button>
      <button @click.prevent="playSound(require('../assets/sounds/no.mp3'))">no</button>
      <button @click.prevent="playSound(require('../assets/sounds/ok_its_really_me.mp3'))">ok it's me</button>
      <button @click.prevent="playSound(require('../assets/sounds/really_question.mp3'))">really?</button>
      <button @click.prevent="playSound(require('../assets/sounds/schedule_followup.mp3'))">follow-up?</button>
      <button @click.prevent="playSound(require('../assets/sounds/wait_what.mp3'))">wait what</button>
      <button @click.prevent="playSound('http://soundbible.com/mp3/Elevator Ding-SoundBible.com-685385892.mp3')">ding</button>
      <button @click.prevent="playSound('http://soundbible.com/mp3/Air Plane Ding-SoundBible.com-496729130.mp3')">dong</button>
    </div>
    <!-- <div class="layer" id="maintenance"> -->

    <!-- </div> -->
  </div>

</template>

<script>
module.exports = {
  methods: {
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
  width: 40em;
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
