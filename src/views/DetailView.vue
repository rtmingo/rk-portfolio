<template>
  <main>
  <div class="about">
    <section v-if="'auflassen' === id">
      <article>
        <img src="../../public/img/big-bang/IMG_0398.jpg" alt="">
        <div class="row">
          <div class="column">
            <h3 style="line-height: 20px;">AUFLASSEN <span style="font-weight: 300">(2022)</span><br>
              <span style="font-weight: 300; font-size: 14px;">Acrylic, spray, and oil stick on cardboard, 100x70</span>
            </h3>
              <p style="font-weight: 300; font-size: 14px; line-height: 28px;">
                os teus pêlos da barba <span style="display: block; font-weight: 200; font-size: 12px;">your bristles <br></span>
                enroscavam entre meus dedos<span style="display: block; font-weight: 200; font-size: 12px;">tangled between my fingers<br></span>
                enquanto te encarava<span style="display: block; font-weight: 200; font-size: 12px;">as I stared at you<br></span>
                como quem não comia há décadas<span style="display: block; font-weight: 200; font-size: 12px;">like someone who hadn't eaten in decades <br></span><br>
                e teu olhar era um mar de água salgada<span style="display: block; font-weight: 200; font-size: 12px;">and your gaze was a sea of salt water <br></span>
                e teu corpo era um oceano<span style="display: block; font-weight: 200; font-size: 12px;">and your body was an ocean <br></span>
                e tua nuca era um perfume<span style="display: block; font-weight: 200; font-size: 12px;">and your scruff was a perfume <br></span>
                e teu sorriso era um sorriso<span style="display: block; font-weight: 200; font-size: 12px;">and your smile was a smile <br></span>
                e teu corpo fez-se mar-aberto<span style="display: block; font-weight: 200; font-size: 12px;">and your body became an open sea<br></span><br>
                pronto a mergulhar <span style="display: block; font-weight: 200; font-size: 12px;">ready to dive</span>
                então mergulhei <span style="display: block; font-weight: 200; font-size: 12px;">so I dove in</span>
              </p>
          </div>
          <div class="column">
            <div class="collage">
              <h3>A closer look</h3>
              <div></div>
              <!-- Images go here -->
              <img src="../../public/img/big-bang/IMG_0401.jpg" alt="Image 1">
              <img src="../../public/img/big-bang/IMG_0407.jpg" alt="Image 3">
              <img src="../../public/img/big-bang/IMG_0409.jpg" alt="Image 2">
              <img src="../../public/img/big-bang/IMG_0399.jpg" alt="Image 2">
            </div>
          </div>
        </div>
      </article>
    </section>
  </div>
</main>
</template>

<style>
.row {
  display: flex;
}

.column {
  flex: 1;
}

article img {
  max-width: 100%;
}

@media (max-width: 845px) {
  .row {
    flex-direction: column;
  }
}
</style>
<script>
export default {
  name: 'DetailView',
  props: {
    id: {
      type: String,
      required: true
    }
  }
}
</script>