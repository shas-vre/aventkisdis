<template>
<div>

  <b-img-lazy :src="imgsrc"></b-img-lazy>

</div>
</template>

<script>
export default {
  props : {
    imgsrc: String,

  } ,
  name: "Textimage"
}
</script>

<style scoped>

</style>