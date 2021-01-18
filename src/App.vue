<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  #app {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  @media screen and (min-Width: 1200px) {
    html{
      font-size: 1px;
    }
  }
  @media screen and (min-Width: 992px) and (max-width: 1199px) {
    html{
      font-size: 0.8px;
    }
  }
  @media screen and (min-Width: 768px) and (max-width: 991px) {
    html{
      font-size: .6px;
    }
  }
  @media screen and (max-width: 767px) {
    html{
      font-size: .4px;
    }
  }
</style>
