<template>
  <div class="column">
    <transition name="flip" mode="out-in">
      <div v-if="!flipped" key="card-front" class="card" @click="flipped = true">
        <div class="card-image">
          <figure class="image is-square is-marginless">
            <img :src="coverImageUrl" alt="Hobby Cover Image">
          </figure>
        </div>
        <header class="card-header">
          <p class="card-header-title has-text-grey">
            {{ hobby.title }}
          </p>
        </header>
      <!-- <div class="card-content">
        <div class="content has-text-centered">
          <p>hello world</p>
        </div>
      </div>
      <footer class="card-footer">
        <div class="card-footer-item">
          <span>
            <slot />
          </span>
        </div>
      </footer> -->
      </div>
      <div v-else key="card-back" class="card" @click="flipped = false">
        <div class="card-content">
          <div class="content">
            {{ hobby.description }}
          </div>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  props: {
    hobby: {
      type: Object,
      required: true
    }
  },
  data () {
    return {
      flipped: false
    }
  },
  computed: {
    coverImageUrl () {
      return require('../assets/' + this.hobby.coverImg)
    }
  }
}
</script>

<style scoped>
.card {
  cursor: pointer;
}

.flip-enter, .flip-leave-to {
  transform: rotateY(90deg);
}

.flip-enter-to, .flip-leave {
  transform: rotateY(0deg);
}

.flip-enter-active, .flip-leave-active {
  transition: transform 0.2s;
}
</style>
