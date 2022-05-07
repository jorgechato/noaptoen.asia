<template>
  <nuxt-link :to="'/'" class="logo">

    <div class="logo__top">
      <div class="small">NO</div>
      APTO
    </div>

    <div class="logo__mid small">EN</div>

    <Parallax
      thumbnail="/japan.png"
      class="logo__bottom">
    </Parallax>

    <div class="logo__bottom front">SI</div>

    <Parallax
      thumbnail="/seoul.png"
      class="logo__bottom">
    </Parallax>

  </nuxt-link>
</template>

<script>
import Parallax from '~/components/Header/Parallax'

export default {
  name: 'Logo',
  props: {
    country: {
      type: String,
      required: false,
    },
    thumbnail: {
      type: String,
      required: false,
    },
  },
  components: {
    Parallax,
  },
  methods: {
    isMobile() {
      if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        return true
      } else {
        return false
      }
    }
  }
}
</script>

<style lang="scss" scoped>

.logo {
  margin: .5em auto .6em auto;
  font-family: "futura-bold";
  text-align: center;
  font-size: 5em;
  display: block;
  text-decoration: none;
  max-width: 400px;
  width: 100%;

  .circle {
    width: .8em;
    height: .8em;
    padding: 0;
    font-size: 1em;
    border-radius: 50%;
    background: white;
    display: inline-block;
  }

  .location {
    font-size: .15em;
    color: grey;
  }

  .logo__top {
    margin-bottom: -15px;
    .small {
      font-size: .7em;
      margin-bottom: -15px;
    }
  }

  .logo__bottom {
    vertical-align: middle;
    display: inline-block;
    font-size: 1.2em;
  }

  .logo__mid {
    font-size: .4em;
    margin-bottom: -15px;
  }

  .front {
    position: relative;
    z-index: 1;
  }
}

</style>
