<template>
  <div>
  <Navigation/> 
  <Home/>
  <Footer/> 
  </div> 
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
<style>
  .page-enter-active,
  .page-leave-active {
    transition-property: opacity;
    transition-timing-function: ease-in-out;
    transition-duration: 500ms;
  }

  .page-enter,
  .page-leave-to {
    opacity: 0;
  }
</style>