<template>
  <div>

    <my-logo/>

      <h2>El podcast</h2>

      <div class="txt">
        <p>
          Bienvenido a "No apto en Asia", el podcast de Jorge Chato.</br>
          Actualidad, anécdotas, curiosidades, debates en Japón, Corea, Tailandia...</br>
          Todas las semanas relato mi descenso a la cultura Asiática, sus costumbres y demonios.
        </p>

        <p>
          He vivido en Corea en plena pandemia y ahora me encuentro en Japón.</br>
          Explorando, desde la curiosidad, todo lo que puede ofrecer.</br>
          ¡Acompáñame y descubramos esto juntos!
        </p>
      </div>

    <social />

      <div>
        <iframe
          class="video"
          src="https://www.youtube.com/embed/videoseries?list=PL6pncPUmit7yWNr_a60flHY2CwB60uvsE"
          frameborder="0">
        </iframe>
      </div>

      <div>
        <iframe
          allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
          width="95%"
          style="border-radius:12px;max-width:660px;min-height:155px;"
          frameBorder="0"
          allowfullscreen=""
          src="https://open.spotify.com/embed/show/7D9vcr6guIw20F4oIe6Dux?utm_source=generator&theme=0">
        </iframe>
      </div>

      <book-list :books="books"/>

  </div>
</template>

<script>
import Nav from '~/components/Header/Nav'
import Logo from '~/components/Header/Logo'
import Next from '~/components/Location/Next'
import BookList from '~/components/Books/List'
import Social from '~/components/Social'

import books from '~/static/books.json'


export default {
  components: {
    'nav-bar': Nav,
    'my-logo': Logo,
    'book-list': BookList,
    'social': Social,
  },
  async asyncData({ $axios }) {
    return {
      books: books,
    }
  }
}
</script>

<style lang="scss" scope>
h2 {
  margin-bottom: 2em;
}

.txt {
  margin: 0 8px;
}

.location-txt {
  h2 {

    a {
      transition: all .1s ease-in-out;

      &:hover {
        font-size: 1.05em;
      }
    }
  }
}

.video {
  aspect-ratio: 16/9;
  width: 100%;
  margin: 2em auto;
}

@media (min-width: 950px) {
  .video {
    width: 70%;
  }
}

@media (min-width: 1280px) {
  .video {
    width: 60%;
  }
}
</style>
