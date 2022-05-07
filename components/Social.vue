<template>
  <div class="social">
    <span class="limit">{</span>

    <a href="http://youtube.jorgechato.com"><fa :icon="['fab', 'youtube']" /></a>
    <a href="http://podcast.jorgechato.com"><fa :icon="['fab', 'spotify']" /></a>
    <a href="http://instagram.jorgechato.com"><fa :icon="['fab', 'instagram']" /></a>
    <a href="http://twitter.jorgechato.com"><fa :icon="['fab', 'twitter']" /></a>

    <span class="limit">}</span>
  </div>
</template>

<script>
export default {
  name: 'Social'
}
</script>

<style lang="scss" scoped>
$youtube: #ff0000;
$spotify: #1db954;
$podcast: #1db954;
$stream: #6441a5;
$instagram: #c13584;
$twitter: #1DA1F2;
$shopping-cart: #034EA2;
$color: rgba(#111, .1);


.svg-inline--fa{
  font-size: 2em;
  padding: 0 .2em;
  text-decoration: none;
  color: $color;
}

.fa-twitter:hover{
  color: $twitter;
}

.fa-youtube:hover{
  color: $youtube;
}

.fa-shopping-cart:hover{
  color: $shopping-cart;
}

.fa-spotify:hover, .fa-podcast:hover{
  color: $spotify;
}

.fa-stream:hover{
  color: $stream;
}

.fa-instagram:hover{
  color: $instagram;
}

  .limit{
    font-size: 3em;
    color: $color;
  }
</style>

