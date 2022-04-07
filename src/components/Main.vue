<template>
  <main class="position-relative">
      <img id="jumbo-overlay" class="w-100 h-50 position-absolute bottom-0" src="../assets/img/jumbo-overlay.svg" alt="jumbo-overlay">
      
  </main>
</template>

<script>
export default {
    name: 'mainIndex',

}
</script>

<style lang="scss" scoped>
@import '../assets/style/_variables.scss';

main{
    width: 100%;
    height: 500px;
    background-color: $brandPrimary;

    img#jumbo-overlay{
        transform: rotate(180deg);
        transform: scaleY(-1);
    }
}

</style>