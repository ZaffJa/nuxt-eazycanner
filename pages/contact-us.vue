<template>
  <div class="container-fluid">
    <Notification :toast="toast" />
    <div class="row">
      <div class="col-sm-12 p-0">
        <GmapMap :center="center" :map-type-id="mapTypeId" :zoom="16">
          <GmapMarker
            v-for="(item, index) in markers"
            :key="index"
            :position="item.position"
            @click="center=item.position"
          />
        </GmapMap>
      </div>
    </div>
    <div class="row w-75 m-auto pt-5">
      <div class="col-sm-4">
        <h3>
          <strong>Head Office</strong>
        </h3>
        <p>
          <span>Eazy Canner Sdn Bhd</span>
          <span>16 Lorong 5,</span>
          <span>Jalan Sentosa, Kampong Dato Onn,</span>
          <span>80350, Johor Bahru, Johor</span>
          <span>Malaysia</span>
        </p>
        <div>“Operating Hours: Opens Daily From 9.00am – 6.00pm”</div>
        <div>+018-870 2422</div>
        <div>www.eazycanner.com</div>
        <div>rahman@eazycanner.com</div>
      </div>
      <div class="col-sm-8">
        <form @submit.prevent="submitForm">
          <div class="row">
            <div class="col-md-6 col-sm-12">
              <input v-model="name" type="text" class="form-control" placeholder="Name">
              <input v-model="email" type="text" class="form-control mt-2" placeholder="Email">
              <input v-model="subject" type="text" class="form-control mt-2" placeholder="Subject">
            </div>
            <div class="col-md-6 col-sm-12">
              <textarea
                v-model="message"
                class="form-control text-dark"
                rows="5"
                placeholder="Message"
              />
            </div>
          </div>
          <button
            type="submit"
            class="btn btn-info btn-lg mt-2 col-sm-12 cursor-pointer"
          >
            SEND MESSAGE
          </button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import Notification from './../components/Notification'

export default {
  components: {
    Notification
  },
  data() {
    return {
      center: { lat: 1.4919, lng: 103.74329 },
      mapTypeId: 'terrain',
      markers: [{ position: { lat: 1.4919, lng: 103.74329 } }],
      name: null,
      email: null,
      message: null,
      subject: null,
      toast: {
        type: '',
        text: ''
      }
    }
  },
  methods: {
    submitForm() {
      this.name = null
      this.email = null
      this.message = null
      this.subject = null
      this.$axios
        .get('https://my-json-server.typicode.com/typicode/demo/posts')
        .then(res => {
          this.toast = {
            text: 'Your request has been submitted successfully',
            type: 'success'
          }
        })
        .catch(ex => {
          this.toast = {
            text: 'An Unexpected error has occured',
            type: 'danger'
          }
        })
    }
  }
}
</script>

<style scoped>
.vue-map-container {
  height: 450px;
  width: 100%;
}
</style>
