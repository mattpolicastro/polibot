# SoundBlasterBlaster

A simple soundboard generator. See a demo [here](https://mattpolicastro.github.io/soundblasterblaster/).

## Project setup

_You should be able to get by with the `npm` equivalents of the commands below if that's your kind of thing, but please submit an issue if that's not the case._

It's generally recommended to have [`vue-cli`](https://cli.vuejs.org/guide/installation.html) installed globally in your development environment to get things going.

```
yarn install
```

### Adding clips

The soundboard points to two sample clips for demonstration purposes when there aren't any files loaded, but it's easy to add your own. Drop your audio files in the `src/assets/sounds/` folder (named with either spaces or underscores) and they should generally take care of themselves. Sorting is arbitrary.

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Deploy
Check the Vue.js [Configuration Reference](https://cli.vuejs.org/config/) and [Deployment](https://cli.vuejs.org/guide/deployment.html#general-guidelines) guides. Once you've created `deploy.sh` (the provided `sample_deploy.sh` is written for GitHub Pages) and updated `vue.config.js` with your project's public-facing GitHub Page path, you should be able to push things live.

```
yarn deploy
```

## Background

In October of 2020 I was leaving a job and wanted to leave behind a landmark to all the shenanigans I got up to with a [virtual soundboard](https://rogueamoeba.com/farrago/) on team calls. I'd also been itching to start writing some code again so I used this as a chance to brush up on Vue.js and general know-how. There's plenty of improvements that can be made here (easier configurability, namely) but for now I'm just working on getting it to being a drop-in solution.