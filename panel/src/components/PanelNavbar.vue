<template>
  <div class="navbar-kapsayici">
    <div>
      <router-link to="/oyuncu-siralamasi"> {{ ilk }} </router-link>
    </div>
    <div>Clan Sıralaması</div>
    <div>
      <img src="https://i.imgur.com/Q0ZQZ8l.png" alt="">
    </div>
    <div>Rehber</div>
    <div>Pus</div>
  </div>
</template>

<script>
export default {
  props: {
    ilk: String
  }
}
</script>

<style>
  .navbar-kapsayici {
    height: 80px;
    background-color: black;
    color: white;
    width: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .navbar-kapsayici > div {
    text-transform: uppercase;
  }

  .navbar-kapsayici > div > a {
    color: white;
    text-decoration: none;
  }
</style>