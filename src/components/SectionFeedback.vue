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
                <p class="p">We work intensively in search of ideals that can add up in the lives of our customers. This is what moves us and we are grateful for the recognition.</p>
          </div>
          <!-- bottom -->
          <ul class="width-100 flex justify_content-space-beetween">
              <li class="card" v-for="(feedback, index) in feedbacks" :key="index">
                <img :src="require('../assets/img/logo-1.png')" alt="logo">
                <p>{{ feedback.text }}</p>
                <p>{{ feedback.conc }}</p>
                <i class="fas fa-quote-right icon-note"></i>
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
                    logo: "require('/assets/img/logo-1.png')",
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad dolorem molestiae eveniet in minima labore cumque vero dolorum porro unde.",
                    conc: "We are continually focused on developing technology solution adapted to our client´s needs."
                },
                {
                    logo: '../assets/img/logo-1.png',
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad dolorem molestiae eveniet in minima labore cumque vero dolorum porro unde.",
                    conc: "We are continually focused on developing technology solution adapted to our client´s needs."
                },
                {
                    logo: '../assets/img/logo-1.png',
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
                font-size: 1.5em;
                position: absolute;
                bottom:25px;
                right:20px;
                color: rgb(75, 75, 75);
            }
            p {
                margin-top: 1em;
            }
        }
    }
}
</style>