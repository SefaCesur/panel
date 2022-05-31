<template>
  <div class="siralama">
    <panel-navbar ilk="sefa cesur"/>
    <h1>Oyuncu Sıralaması Sayfası</h1>
    <div>
      {{
        entry.data.text
      }}
      - yazar: <b>{{ entry.data.user.username }}</b>
      <br> {{ entry.data.created_at }}
    </div>
    <br><br>
    <div :key="index" v-for="(price, index) in prices">
      {{ price.symbol }} : {{ price.price }} <br>
    </div>
    </div>
</template>

<script>
import PanelNavbar from '../components/PanelNavbar.vue';

export default {
  name: 'SiralamaView',
  components: {
    'panel-navbar': PanelNavbar
  },
  data() {
    return {
      links: ['Clan Sıralaması', 'Player Sıralaması', 'Upgrade Oranları', 'Power Up Store'],
      prices: [],
      entry: {}
    }
  },
  methods: {
  },
  async created() {
    const response = await fetch('https://api.binance.com/api/v3/ticker/price');
    const jsonResponse = await response.json();

    const entryResponse = await fetch('https://sausozluk.net/service/proxy/api/v1/entries/3818');
    const entryResponseJson = await entryResponse.json();

    this.entry = entryResponseJson;
    this.prices = jsonResponse;
  }
}
</script>

<style>

</style>