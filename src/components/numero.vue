<template>
<div id="id" >


  <b-img v-if="currentdate < date" fluid :src="imgsrc"></b-img>

  <b-img v-if="(currentdate > date) || (isopen === true)" fluid :src="imgend" data-toggle="modal" :data-target="'.bd-example-modal-xl'+date"></b-img>


  <b-img v-else-if=" (currentdate === date )||  (isopen === false)"  fluid :src="imgsrc" data-toggle="modal" :data-target="'.bd-example-modal-xl'+date" @click="opening()"></b-img>

  <div  :class="'modal justify-content-center fade bd-example-modal-xl'+date" tabindex="-1" role="dialog" aria-labelledby="myLargeModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-xl">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">Conseil du jour </h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <b-img fluid :src="imgmodal"  :key="imgmodal"></b-img>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      isopen: false,

    }
  },
  mounted() {
    var tmp = new Date();
    this.currentdate =tmp.getDate();
    console.log(this.isopen + 'mounting');
    console.log('Image Modal',this.imgmodal);
  },


  methods:{
    opening(){
      console.log(this.isopen +'opening');
      this.isopen = true;
      console.log(this.isopen)
    }

  },

  props : {
    imgmodal: String,
    imgsrc: String,
    imgend: String,
    date: String,
    currentdate: String,


  } ,
  name: "Textimage"
}

</script>

<style scoped>

</style>