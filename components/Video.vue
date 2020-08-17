
<template>
  <div class="video">
    <div class="section-title text-center">
      <Title class="main-title" big bold sky title="التميز في العناية بالعيون" />
    </div>
    <div class="video__img relative">
      <b-img-lazy src="../assets/images/building.jpg" class="video__bg" fluid-grow></b-img-lazy>
      <div class="video__img__overlay">
        <div class="video__img__overlay__text text-center">
          <Title medium white bold title="لأنهم أملنا ومستقبلنا" />
          <Title medium white bold title="نهتم دائما بحماية ورعاية أعينهم" />
          <div v-b-modal.modal-center>
            <b-img-lazy src="../assets/images/icons/video.svg" class="play-img"></b-img-lazy>
          </div>

          <b-modal id="modal-center" size="lg" centered hide-footer>
            <iframe
              width="560"
              height="315"
              src="https://www.youtube.com/embed/tZQNPCWkp8A"
              frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </b-modal>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Title from "./Title";

export default {
  name: "Video",

  components: {
    Title,
  },
};
</script>

<style scoped>
.video {
  background: url("../assets/images/little-eye.png");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center left;
}

.video__img .video__img__overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: rgba(0, 149, 175, 0.5);
  padding: 3rem 0;
}

.video__img__overlay__text img {
  width: 200px;
  margin-top: 2rem;
}

iframe {
  width: 100% !important;
  height: 300px !important;
}

@media (min-width: 992px) and (max-width: 1183px) {
  .play-img {
    width: 90px !important;
  }
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 320px) and (max-width: 767px) {
  .video {
    background-size: cover;
  }
  .video__bg {
    height: 300px !important;
    -o-object-fit: cover;
    object-fit: cover;
  }
  .video__img img {
    height: 100px;
  }
  .video__img .video__img__overlay {
    padding: 1rem 0;
  }
}
</style>