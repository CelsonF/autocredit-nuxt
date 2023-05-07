<template>
  <div class="glide my-4">
    <div class="glide__track" data-glide-el="track">
      <ul class="glide__slides">
        <li class="glide__slide"><img
            src="https://upload.wikimedia.org/wikipedia/commons/e/e8/Logo_Receita_Federal_do_Brasil.svg"></li>
        <li class="glide__slide"><img src="~/assets/images/denatran.svg"></li>
        <li class="glide__slide"><img src="~/assets/images/serpro.svg"></li>
        <li class="glide__slide"><img src="~/assets/images/miniteriodafazenda.svg"></li>
      </ul>
    </div>
  </div>
</template>

<script>
import Glide from '@glidejs/glide/dist/glide.esm'

export default {
  name: 'Slide',
  mounted() {
    const glide = new Glide('.glide', {
      type: 'carousel',
      perView: 4,
      autoplay: 2000,
    });
    glide.mount();
  },
}
</script>

<style>
.glide {
  width: 100%;
  height: 6rem;
  overflow: hidden;
}

.glide__track {
  height: 100%;
}

.glide__slides {
  height: 100%;
  display: flex;
  list-style: none;
}

.glide__slide {
  height: 100%;
  width: 100%;
  flex-shrink: 0;
}

.glide__slide img {
  height: 100%;
  width: 100%;
  object-fit: contain;
  filter: grayscale(1);
  transform:  scale(0.75);
}

</style>