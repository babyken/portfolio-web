<template>
  <div class="container">
    <page-header :title="'Programming Experience'" />
    <div class="content">
      <h3 class="title is-3">
        2020 - Present
      </h3>
      <ul>
        <li>Study and play around the basic of Flutter</li>
        <li>Study vuejs for building more fancy website</li>
      </ul>
      <h3 class="title is-3">
        2016 - 2019
      </h3>
      <ul>
        <li>Develop plugins and modify ePlatform - Moodle and OpenEdx</li>
        <li>Built <a href="https://gift.fed.cuhk.edu.hk/" target="_blank">Project website</a> and CMS with Laravel and bootstrap</li>
      </ul>
      <h3 class="title is-3">
        2011 - 2015
      </h3>
      <ul>
        <li>FYP Project iOS program on iPhone 3GS with bluetooth communication</li>
        <li>Mini Unity3D project with Unity Script</li>
        <li>Microsoft surface table project on CSL Flagship store</li>
        <li>Online Movie steaming service - <a href="https://www.hermeslive.com/">Hermes</a></li>
        <li>An iOS violin tuner app for primary students</li>
        <li>
          iOS Apps for
          <a href="https://apps.apple.com/us/app/hypebeast/id986768161" target="_blank">Hypebeast</a>,
          <a href="https://apps.apple.com/us/app/popbee/id1022028083" target="_blank">Popbee</a> and
          <a href="https://apps.apple.com/us/app/hbx-globally-curated-fashion/id895353739" target="_blank">Hypebeast store</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import PageHeader from '@/components/PageHeader'
export default {
  components: {
    PageHeader
  },
  transition: 'slide-left'
}
</script>

<style>

</style>
