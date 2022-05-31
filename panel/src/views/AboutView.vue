<template>
  <div class="about">
    <panel-navbar/>
  </div>
</template>

<script>
import PanelNavbar from '../components/PanelNavbar.vue'

export default {
  name: 'AboutView',
  components: {
    'panel-navbar': PanelNavbar
  }
}
</script>