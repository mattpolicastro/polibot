<template>
  <div>
    <img alt="Polibot" src="../assets/polibot.png" id="polibot">
    <h1>polibot keeps it wavy</h1>
    <i>~ y o u ~ k n o w ~ t h e ~ v i b e s ~</i>
  </div>
</template>

<style>
#polibot {
  max-width: 24em;
  margin: auto;
  display: inline-block;
  animation: rotation 1.2s infinite ease;
  transform: rotate(-15deg);
}
h1 {
  font-weight: 800;
  margin-bottom: 0;
}
i {
  font-weight: 400;
}
@keyframes rotation {
  50% {
    transform: rotate(15deg);
  }
}
</style>
