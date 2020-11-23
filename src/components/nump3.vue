<!--
<template>
  <div>


    <b-img v-if="currentdate >= date" fluid :src="imgsrc"></b-img>

    <b-img v-else-if="isopen == false"  fluid :src="imgsrc" data-toggle="modal" data-target=".bd-example-modal-lg" @click="opening()"></b-img>
    <b-img v-else-if="isopen == true" fluid src="https://via.placeholder.com/300" data-toggle="modal" data-target=".bd-example-modal-lg"></b-img>

    <div class="modal fade bd-example-modal-lg" tabindex="-1" role="dialog" aria-labelledby="myLargeModalLabel" aria-hidden="true">
      <div class="modal-dialog modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel">Conseil du jour MP3</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <b-img fluid src="http://noah.test.kisdis.com/img/1-12.495b2f69.jpg"></b-img>
          </div>
          <div class="modal-footer align-content-center">
            <audio controls >
              <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_1MG.mp3" type="audio/mpeg">
            </audio>
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

  },


  methods:{
    opening(){
      console.log(this.isopen +'opening');
      this.isopen = true;
      console.log(this.isopen)
    }

  },

  props : {
    imgsrc: String,
    date: String,
    currentdate: String,


  } ,
  name: "nump3"
}

</script>

<style scoped>

</style>-->
