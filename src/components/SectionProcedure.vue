<template>
  <section class="SectionProcedure container width-100 flex">
      <div class="width-100 margin-auto flex flex-direction-column">
          <!-- top -->
          <div class="top width-60 margin-auto flex flex-direction-column align-items-center">
                <h3 class="h3">HOW IT WORKS IN PRACTICE</h3>
                <h2 class="h2">
                    <span class="color">Logistical</span>
                    <span> Procedure</span>
                </h2>
                <p class="p">With all of this exprtise and capability comes an unrivalled commitment to customer service. We will work hard to understand your needs in order to develop a productive, long-term partnership.</p>
          </div>
          <!-- bottom -->
          <ul class="width-100 flex justify_content-center">
              <li v-for="(procedure, index) in procedures" :key="index">
                  <div class="number-procedure">{{ "0" + (index + 1) }}</div>
                  <div class="procedure flex flex-direction-column">
                      <h5>{{ procedure.name }}</h5>
                      <p>{{ procedure.info }}</p>
                  </div>
              </li>
          </ul>
      </div>
  </section>
</template>

<script>
export default {
    name:"SectionProcedure",
    data() {
        return {
            procedures: [
                {
                    name: "Collection of information",
                    info: " Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    name: "Collection of information",
                    info: " Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    name: "Collection of information",
                    info: " Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    name: "Collection of information",
                    info: " Lorem ipsum dolor sit amet consectetur adipisicing elit."
                },
                {
                    name: "Collection of information",
                    info: " Lorem ipsum dolor sit amet consectetur adipisicing elit."
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
    background-color: $third-color-bg-section;
    // top
    .top {
        h2 {
            color: $fourth-color-text;
            .color {
                color: $third-color-text;
                background-color: $color-bg-title;
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
        padding: 0 5em;
        margin-top: 4em;
        border-top: 4px solid $color-bg-title;
        li {
            flex-basis: calc((100% / 5) - 20px);
            position: relative;
            .number-procedure {
                padding: 0.5em;
                font-size: 1em;
                font-weight: 800;
                background-color: $color-bg-title;
                border-radius: 50%;
                color: $third-color-text;
                position: absolute;
                top:-20px;
                left:45%;
            }
            h5 {
                margin: 1em 0 0.5em 0;
                font-size: 1.5em;
                color: $fourth-color-text;
                text-align: center;
            }
            p {
                text-align: center;
            }
        }
    }
}
</style>