<template>

        <div class="card"
          :style="{ backgroundImage: 'url(' + thumbnail + ')' }">
        </div>

</template>

<script>
import Parallax from '~/components/Header/Parallax'

export default {
  name: 'MicroLogo',
  props: {
    thumbnail: {
      type: String,
      required: true,
    },
  },
  components: {
    Parallax,
  },
}
</script>

<style lang="scss" scoped>
$mainColor: white;


.card {
  position: relative;
  flex: 0 0 240px;
  width: 1.4em;
  height: 1.2em;
  background-color: #333;
  overflow: hidden;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  z-index: -1;
  margin: 10px -35px;
}

.card:after{
  content: ' ';
  border-style: solid;
  border-width: 0 .455em 1.2em .45em;
  border-color: $mainColor $mainColor transparent $mainColor;
  position: absolute;
  width: .5em;
  left: 0;
  top: 0;
  right: 0;
}

.logo__min {
  font-family: "futura-bold";
  font-size: 1.5em;
  display: block;
  text-decoration: none;
  float: left;
  color: white;

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
    font-size: 1.1em;
    margin-bottom: -15px;
  }

  .logo__bottom {
    vertical-align: middle;
    display: inline-block;
  }

  .front {
    position: relative;
    z-index: 1;
  }
}

</style>
