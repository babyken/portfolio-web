<template>
  <aside class="menu">
    <ul class="menu-list">
      <li>
        <figure class="profile image is-128x128">
          <img class="is-rounded" src="~/assets/ken_profile.png" alt="profile pic">
        </figure>
      </li>
      <li v-for="(item, key) of items" :key="key">
        <nuxt-link
          :to="item.to"
          exact-active-class="is-active"
        >
          <b-icon :icon="item.icon" />
          {{ item.title }}
        </nuxt-link>
      </li>
    </ul>
  </aside>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      required: true
    }
  },
  transitions: 'slide-left'
}
</script>

<style scoped>
/*menu bar */
figure.profile {
    margin: 15px auto 25px auto;
}

figure.profile {
    animation: rotate 2s ease forwards;
    animation-play-state:paused;
}
figure.profile:hover {
    animation-play-state: running;
}

.menu-list a:not(.is-active):hover {
    animation: flash 0.8s forwards;
}

.menu-list a.is-active {
    background-color: #437c92;
}

@keyframes flash {
    0% {
        background: transparent;
    }
    50% {
        background: #f5f5f5;
    }
    100% {
        background: #e8f7fe;
    }
}

@keyframes rotate {
    0% {transform: rotate(38deg);}
    25% {transform: rotate(-12deg);}
    75% {transform: rotate(14deg);}
    100% {transform: rotate(0deg);}
}
</style>
