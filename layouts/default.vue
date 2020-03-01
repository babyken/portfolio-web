<template>
  <div class="main container">
    <section class="columns">
      <div class="column is-3">
        <app-side-menu :items="items" />
      </div>
      <div class="column is-9">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
import SideMenu from '@/components/SideMenu'
export default {
  components: {
    appSideMenu: SideMenu
  },
  data () {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Code Log',
          icon: 'code-tags',
          to: { name: 'code-log' }
        }, {
          title: 'Hobby',
          icon: 'guitar-acoustic',
          to: { name: 'hobby' }
        }

      ]
    }
  },
  head () {
    return {
      title: 'About Ken Hui'
    }
  }
}
</script>

<style>
@media only screen and (max-width: 768px) {
  .main.container {
    padding: 12px;
  }
}

@media only screen and (min-width: 769px) {
  .main.container {
    margin: 30px auto;
    padding: 8px;
    padding-bottom: 15px;
    background-color: #fbfbfb;
    border-radius: 25px;
  }
}

@media only screen and (min-width: 1025px) {
  .main.container {
    margin: 100px 130px;
    padding: 40px;
    padding-bottom: 70px;
    background-color: #fbfbfb;
    border-radius: 25px;
  }
}

</style>
