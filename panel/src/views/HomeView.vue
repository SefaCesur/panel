<template>
  <div class="home">
    <panel-navbar ilk="oyuncu siralamasi"/>
  </div>
</template>

<script>
import PanelNavbar from '../components/PanelNavbar.vue';

export default {
  name: 'HomeView',
  components: {
    'panel-navbar': PanelNavbar
  },
  data() {
    return {
      links: ['Clan Sıralaması', 'Player Sıralaması', 'Upgrade Oranları', 'Power Up Store']
    }
  },
  methods: {
    selamVerme(playerName) {
      alert('Hoş geldin ' + playerName);
    }
  }
}
</script>

<style>

</style>