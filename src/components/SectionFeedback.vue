<template>
  <section class="section-feedback container width-100 flex">
      <div class="width-60 margin-auto flex flex-direction-column">
          <!-- top -->
          <div class="top width-100 margin-auto flex flex-direction-column align-items-center">
                <h3 class="h3">CUSTOMER TESTIMONIALS</h3>
                <h2 class="h2">
                    <span>Trusted</span>
                    <span class="color"> Feedback</span>
                </h2>
                <p class="p">With all of this exprtise and capability comes an unrivalled commitment to customer service. We will work hard to understand your needs in order to develop a productive, long-term partnership.</p>
          </div>
          <!-- bottom -->
          <ul class="width-100 flex justify_content-space-beetween">
              <li class="card" v-for="(feedback, index) in feedbacks" :key="index">
                <img :src="require('../assets/img/logo-1.png')" :alt="logo-woocommerce">
                <p>{{ feedback.text }}</p>
                <p>{{ feedback.conc }}</p>
                <font-awesome-icon class="icon-note" :icon="['fas', 'user']"/>
              </li>
          </ul>
      </div>
  </section>
</template>

<script>
export default {
    name:"SectionFeedback",
    data() {
        return {
            feedbacks: [
                {
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad dolorem molestiae eveniet in minima labore cumque vero dolorum porro unde.",
                    conc: "We are continually focused on developing technology solution adapted to our client´s needs."
                },
                {
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad dolorem molestiae eveniet in minima labore cumque vero dolorum porro unde.",
                    conc: "We are continually focused on developing technology solution adapted to our client´s needs."
                },
                {
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad dolorem molestiae eveniet in minima labore cumque vero dolorum porro unde.",
                    conc: "We are continually focused on developing technology solution adapted to our client´s needs."
                }
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
    background-color: $second-color-bg-section;
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
        margin-top: 2em;
        .card {
            padding: 2em;
            flex-basis: calc((100% / 3) - 20px);
            background-color: $color-bg-card;
            border-radius: 10px;
            position: relative;
            img {
                width: 150px;
                filter: invert(100%);
            }
            .icon-note {
                position: absolute;
                bottom:25px;
                right:20px;
                color: $third-color-text;
            }
            p {
                margin-top: 1em;
            }
        }
    }
}
</style>