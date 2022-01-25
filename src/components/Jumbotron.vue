<template>
      <!-- JUMBOTRON -->
      <div class="jumbotron width-100">
          <div class="opacity width-100 flex">
              <div class="call-to-action-box width-60 margin-auto flex">
                  <div class="call-to-action">
                      <h2>LOGISTIC SERVICES</h2>
                      <h1>CARGO TRANSPORT</h1>
                      <p>Fractional or exclusive road cargo transportation to all regions, with small, medium and large vehicles.</p>
                      <div class="box-buttons width-100 flex">
                          <button class="button-with-bg">get in touch</button>
                          <button class="button-with-border">read more</button>
                      </div>
                  </div>
              </div>
          </div>

      </div>
</template>

<script>
export default {
    name: "Jumbotron",
}
</script>

<style lang="scss" scoped>
@import "../assets/partials/_common.scss";
@import "../assets/partials/_mixin.scss";
@import "../assets/partials/_variables.scss";

// JUMBOTRON
.jumbotron {
    height: $first-height;
    background-image: url("../assets/img/bg-9.jpg");
    background-size: cover;
    .opacity {
        height: 100%;
        background: rgba(0, 0, 0, 0.5);
        .call-to-action {
            width: 50%;
            h2{
                color: $third-color-text;
                font-size: 0.8em;
            }
            h1 {
                margin-top: 0.2em;
                font-size: 3em;
            }
            p {
                margin: 2em 0;
                color: $second-color-text;
            }
            .button-with-bg {
                margin-right: 1.5em;
            }
        }
    }
}
</style>