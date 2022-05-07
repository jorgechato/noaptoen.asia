<template>
  <div class="footer__net">

    <Social />

    <div class="by">
      con <a href="//github.com/jorgechato/noaptoen.asia"><fa :icon="['fas', 'heart']" /></a> por Jorge Chato
    </div>

  </div>
</template>

<script>
import Social from '~/components/Social'

export default {
  components: {
    Social,
  },
}
</script>

<style lang="scss" scoped>
$textColor: #111;
$color: rgba($textColor, .15);


.footer__net{
  padding-top: 2em;
  padding-bottom: 2em;
  text-align: center;

  .by{
    padding-top: 2em;
    color: rgba($textColor, .1);

    .fa-heart {
      font-size: inherit;
      color: rgba($textColor, .1);

      &:hover {
        font-size: inherit;
        color: rgba(red, .6);
      }
    }
  }

}

.limit, .social {
  display: inline-block;
  vertical-align: middle;
}

.social {
  padding-top: .5em;
}

</style>
