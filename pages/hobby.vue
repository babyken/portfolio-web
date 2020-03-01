<template>
  <div class="container">
    <page-header :title="'Life With Fun'" />
    <div class="content">
      <div class="columns">
        <Card v-for="(hobby, index) in hobbies" :key="index" :hobby="hobby" />
      </div>
    </div>
  </div>
</template>

<script>
import PageHeader from '@/components/PageHeader'
import Card from '@/components/Card'

export default {
  transition: 'slide-left',
  components: {
    PageHeader,
    Card
  },
  data () {
    return {
      hobbies: [{
        title: 'Guitar and Music',
        description: 'I started my music journey since 2012. Music bring the magic through the air. As a dummy in art, I feel like I am an artist while playing my guitar.',
        coverImg: 'guitar_gomans.jpg'
      },
      {
        title: 'World through Lens',
        description: 'Camera could capture a moment of air. I started to play around lens and cameras since 2007. Yea, I agree I was equipment-driven photography. Now I restart my lens story with how to compose a image by heart.',
        coverImg: 'camera_xe2.jpg'
      },
      {
        title: 'A Black Cat',
        description: 'I named her Kuroro, black in Japanese. I adopt her since 2017. She\'s a active, attractive and aloof cat. Some said black cat bring disaster to its master. I said she is a treasure to me',
        coverImg: 'kuroro.jpg'
      }]
    }
  }
}
</script>

<style>

</style>
