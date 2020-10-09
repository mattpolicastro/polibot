<template>
  <div>
    <button @click.prevent="playSound(require('../assets/sounds/hey.mp3'))">Hey</button>
  </div>
</template>

<script>
module.exports = {
  methods: {
    playSound (sound) {
      if(sound) {
        var audio = new Audio('file://'+sound);
        audio.play();
      }
    }
  }
}
</script>
