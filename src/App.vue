<template>
  <div class="nav">
    <h1>The <strong>Big Send</strong> Soundboard</h1>
    <!-- <h1>💪🏼 💌 🙏</h1> -->
  </div>
  <div class="grid">
    <SoundButton name="big send please!" icon="💌" :files="['big-send-kat.mp3', 'big-send-tim.mp3']" />
    <SoundButton name="we're going big today!" icon="💪🏼" :files="['going-big-kat.mp3', 'going-big-tim.mp3']" />
    <SoundButton name="order up!" icon="🆙" :files="['order-up-kat.mp3', 'order-up-tim.mp3']" />
    <SoundButton name="yes chef!" icon="👩‍🍳" :files="['yes-chef-kat.mp3', 'yes-chef-tim.mp3']" />
    <SoundButton name="reverse starfish?" icon="⭐️" :files="['reverse-starfish-kat.mp3', 'reverse-starfish-tim.mp3']" />
    <SoundButton name="crab tickler!" icon="🦀" :files="['crab-tickler-kat.mp3', 'crab-tickler-tim.mp3']" />
    <SoundButton name="slap it!" icon="🖐" :files="['slap-it-kat.mp3', 'slap-it-tim.mp3']" />
    <SoundButton name="toe reveal!" icon="🦶" :files="['toe-reveal-kat.mp3', 'toe-reveal-tim.mp3']" />
  </div>
</template>

<script>
import SoundButton from '@/components/SoundButton.vue';

export default {
  name: 'App',
  components: {
    SoundButton
  }
}
</script>

<style lang="scss">
@font-face {
  font-family: "Montserrat";
  src: local("Montserrat"), url(assets/fonts/Montserrat-Regular.ttf) format("truetype");
}
@font-face {
  font-family: "MontserratBold";
  src: local("Montserrat"), url(assets/fonts/Montserrat-Bold.ttf) format("truetype");
}

* {
  box-sizing: border-box;
}

html {
  height: 100%;
  background: rgb(148,187,233);
}

body {
  font-family: "Montserrat";
  margin: 0;
  background: rgb(148,187,233);
  background: linear-gradient(210deg, rgba(238,174,202,1) 0%, rgba(148,187,233,1) 100%);
}

.nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 60px;
  background: gold;
  display: flex;
  padding: 10px 20px;
  justify-content: space-between;
  background: #94bbe9;
  box-shadow: 0 0 10px 0 black;
  color: white;
  text-align: center;

  h1 {
    margin: auto auto;
    font-size: 1.4rem;
    text-shadow: rgb(238,174,202) 4px 4px;
  }

  strong {
    font-family: "MontserratBold";
  }
}

.grid {
  display: grid;
  grid: auto-flow / 1fr 1fr;
  grid-gap: 1rem;
  padding: 20px;
  margin: 60px 0 0 0;
  overflow: hidden;
  min-height: calc(100vh - 60px);
}
</style>
