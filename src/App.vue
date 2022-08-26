<template>
  <div class="nav">
    <h1>Big Send Please!!</h1>
    <h1>💪🏼 💌 🙏</h1>
  </div>
  <div class="grid">
    <SoundButton name="big send please!" icon="💌" :files="['big-send-kat.m4a', 'big-send-tim.m4a']" />
    <SoundButton name="we're going big today!" icon="💪🏼" :files="['going-big-kat.m4a', 'going-big-tim.m4a']" />
    <SoundButton name="order up!" icon="🆙" :files="['order-up-kat.m4a', 'order-up-tim.m4a']" />
    <SoundButton name="yes chef!" icon="👩‍🍳" :files="['yes-chef-kat.m4a', 'yes-chef-tim.m4a']" />
    <SoundButton name="reverse starfish?" icon="⭐️" :files="['reverse-starfish-kat.m4a', 'reverse-starfish-tim.m4a']" />
    <SoundButton name="crab tickler!" icon="🦀" :files="['crab-tickler-kat.m4a', 'crab-tickler-tim.m4a']" />
    <SoundButton name="slap it!" icon="🖐" :files="['slap-it-kat.m4a', 'slap-it-tim.m4a']" />
    <SoundButton name="toe reveal!" icon="🦶" :files="['toe-reveal-kat.m4a', 'toe-reveal-tim.m4a']" />
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
  font-family: "MontserratBold";
  color: white;

  h1 {
    margin: auto 0;
    font-size: 1.6rem;
    text-shadow: rgb(238,174,202) 4px 4px;
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
