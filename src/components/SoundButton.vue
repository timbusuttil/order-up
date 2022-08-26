<template>
  <div class="button" :style="buttonStyle" @click="play">
    <p class="icon">{{ icon }}</p>
    <p class="label">{{ name }}</p>
  </div>
</template>

<script>
import { Howl } from 'howler';

export default {
  name: 'SoundButton',
  props: {
    name: String,
    icon: String,
    audio: String
  },
  data() {
    return {
      isPlaying: false,
      sound: null
    }
  },
  computed: {
    buttonStyle() {
      return {
        transform: this.isPlaying ? `scale(1.2) rotate(${this.angle}deg)` : '',
        transition: this.isPlaying ? 'transform 0.6s cubic-bezier(0.68, -3, 0.32, 2)' : 'transform 0.6s cubic-bezier(0.68, -1, 0.32, 4)'
      }
    }
  },
  methods: {
    play() {
      if (this.sound === null) this.initSound();
      this.sound.stop();
      this.isPlaying = true;
      this.angle = -30 + Math.floor(Math.random() * 60);
      this.sound.play();
    },
    initSound() {
      this.sound = new Howl({
        src: ['audio/orderup.mp3']
      });
      this.sound.on('end', () => {
        this.isPlaying = false;
      });
    }
  },
}
</script>

<style lang="scss" scoped>
.button {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  // aspect-ratio: 1;
  width: 100%;
  height: 100%;
  min-height: 167px;
  padding: 10px;
  border-radius: 1rem;
  box-sizing: border-box;
  border-style: outset;
  background: rgba(255, 255, 255, 0.3);
  border-width: 3px;

  p {
    margin: 0;
  }

  .icon {
    font-size: 5rem;
  }

  .label {
    font-size: 1.2rem;
    font-family: "Montserrat";
  }
}
</style>
