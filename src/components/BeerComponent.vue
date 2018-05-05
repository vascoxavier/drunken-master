<template>
  <div class="box">
  <article class="media">
    <div class="media-left">
      <figure class="image is-64x64">
        <img :src="beer.image_url" alt="Image">
      </figure>
    </div>
    <div class="media-content">
      <div class="title">{{beer.name}}</div>
      <div class="content">
        {{beer.description}}
        <div>
          <a class="button is-black" @click="showMore">Learn more</a>
        </div>
      </div>
        <div class="modal">

          <div class="modal-background"></div>
          <div class="modal-card">
            <header class="modal-card-head">
              <p class="modal-card-title">Modal title</p>
              <button class="delete" aria-label="close"></button>
            </header>

          <section class="modal-card-body">
              This is my modal
          </section>
          <footer class="modal-card-foot">
            <button class="button is-success">Save changes</button>
            <button class="button">Cancel</button>
          </footer>
        </div>
      </div>
    </div>
  </article>
</div>
</template>

<script>
export default {
  props: {
    beer: {}
  }
}
</script>

<style>

</style>
