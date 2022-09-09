<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <main>
    <section class="container">
      <h1>Vídeos</h1>

      <section class="videos">
        <div class="video" v-for="(video, index) in videos" :key="index">
          <a :href="video.link" target="_blank">
            <img :src="video.thumb" :alt="video.title" />
            <div class="video-title">{{ video.title }}</div>
          </a>
        </div>
      </section>
    </section>
  </main>
</template>

<script>
import api from "@/services/api";
export default {
  data() {
    return { videos: [] };
  },
  mounted() {
    api.get("/videos.json").then(response => {
      this.videos = response.data;
    });
  },
};
</script>

<style scoped>
main {
  align-items: center;
}
.videos {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.video {
  width: 80%;
  margin-bottom: 30px;
}

.video img {
  width: 100%;
}

.video a {
  color: var(--color-text-dark);
  font-weight: 600;
}

@media (min-width: 700px) {
  .videos {
    flex-direction: row;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 30px;
  }

  .video {
    width: 30%;
  }
}
</style>
