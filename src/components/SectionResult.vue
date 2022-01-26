<template>
  <section class="section-result container width-100 flex">
      <div class="width-60 margin-auto flex flex-direction-column">
          <!-- top -->
          <div class="top width-100 margin-auto flex flex-direction-column align-items-center">
                <h3 class="h3">WHAT ARE WE DOING</h3>
                <h2 class="h2">
                    <span class="color">Results</span>
                    <span> in Numbers</span>
                </h2>
          </div>
          <!-- bottom -->
          <ul class="width-100 flex justify_content-space-beetween">
              <li v-for="(result, index) in results" :key="index">
                <h6>{{ result.number }}</h6>
                <h5>{{ result.type }}</h5>
              </li>
          </ul>
      </div>
  </section>
</template>

<script>
export default {
    name:"SectionResult",
    data() {
        return {
            results: [
                {
                    number: 128,
                    type: "Certifications"
                },
                {
                    number: 230,
                    type: "Employees"
                },
                {
                    number: 517,
                    type: "Customers"
                },
                {
                    number: 94,
                    type: "Countries Served"
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/partials/_common.scss";
@import "../assets/partials/_mixin.scss";
@import "../assets/partials/_variables.scss";

.container {
    height: $first-height;
    background-image: url(../assets/img/bg-10.jpg);
    background-position: center;
    // top
    .top {
        h2 {
            color: $first-color-text;
            .color {
                background-color: $color-second-bg-title;
            }
        }
        .p {
            width: 75%;
            text-align: center;
        }
    }
    // bottom
    ul {
        @include list-nav;
        margin-top: 4em;
        h6 {
            font-size: 3em;
            color: $third-color-text;
            text-align: center;
        }
        h5 {
            font-size: 1.5em;
        }
    }
}
</style>