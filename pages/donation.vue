<template>
  <div class="container mt-5">
    <div class="row">
      <div class="col-lg-6">
        <h3 class="text-dark">
          <u>DONATION</u>
        </h3>
        <p>For those who wants to send any cheque or bank draft or money order, kindly post or courier to the address below:</p>
        <p>
          <span>Eazy Canner Sdn Bhd</span>
          <span>16 Lorong 5,</span>
          <span>Jalan Sentosa, Kampong Dato Onn,</span>
          <span>80350, Johor Bahru, Johor</span>
          <span>Malaysia</span>
        </p>
        <p>Maybank Account No: 551593521287</p>

        <p>Kindly call Customer Service at 018 – 870 2422 (e-mail : rahman@eazycanner.com) for any enquiries.</p>

        <p>
          To order please go to this
          <nuxt-link to="/how-to-buy">
            link
          </nuxt-link>and please do not send cash.
        </p>
      </div>
      <div class="col-lg-6">
        <img src="~assets/images/front-machine.jpg" alt class="img-fluid">
      </div>
    </div>
    <div class="row mt-5">
      <div class="col-sm-3 text-center">
        <h4>TEMPERATURE GRAPH</h4>
        <a class="btn btn-info mt-3" href="~static/pdf/graph-data-temperature.pdf">DOWNLOAD</a>
      </div>
      <div class="col-sm-3 text-center">
        <h4>NUTRITIONAL VALUE TEST REPORT</h4>
        <a class="btn btn-info mt-3" href="~static/pdf/nutritional-value-test-report.pdf">DOWNLOAD</a>
      </div>
      <div class="col-sm-3 text-center">
        <h4>MICROBE TEST REPORT</h4>
        <a class="btn btn-info mt-3" href="~static/pdf/microbe-test-report.pdf">DOWNLOAD</a>
      </div>
      <div class="col-sm-3 text-center">
        <h4>PURCHASE ORDER FORM</h4>
        <a class="btn btn-info mt-3" href="~static/pdf/purchase-order.pdf">DOWNLOAD</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
p > span {
  width: 100%;
  display: block;
  color: black;
  padding: 4px 0;
  font-weight: bolder;
  font-size: large;
}
</style>
