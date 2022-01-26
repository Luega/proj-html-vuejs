<template>
  <section class="section-services container width-100 flex">
      <div class="width-60 margin-auto flex flex-direction-column">
          <!-- top -->
          <h3 class="h3">ROAD TRANSPORT</h3>
          <h2 class="h2">
              <span>Main</span>
              <span class="color"> Services</span>
          </h2>
          <div class="flex width-100 justify_content-space-beetween">
              <p class="p">With all of this exprtise and capability comes an unrivalled commitment to customer service. We will work hard to understand your needs in order to develop a productive, long-term partnership.</p>
              <button class="button-with-border">see all</button>
          </div>
          <!-- bottom -->
          <ul class="width-100 flex justify_content-space-beetween">
              <li class="card" v-for="(service, index) in services" :key="index">
                  <a href="#">
                    <font-awesome-icon class="icon-service" :icon="['fas', 'user']"/>
                    <font-awesome-icon class="icon-arrow" :icon="['fas', 'user']"/>
                    <h4>{{ service.name }}</h4>
                    <p>{{ service.info }}</p>
                  </a>
              </li>
          </ul>
      </div>
  </section>
</template>

<script>
export default {
    name:"SectionServices",
    data() {
        return {
            services: [
                {
                    name: "Technology",
                    info: "We are continually focused on developing technology solution adapted to our client´s needs."
                },
                {
                    name: "Reefer Cargo",
                    info: "We are continually focused on developing technology solution adapted to our client´s needs."
                },
                {
                    name: "Dry Cargo",
                    info: "We are continually focused on developing technology solution adapted to our client´s needs."
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
    h2 {
        color: $first-color-text;
        .color {
            background-color: $color-second-bg-title;
        }
    }
    .p {
        width: 75%;
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
            cursor: pointer;
            .icon-service {
                width: 60px;
                height: 60px;
                padding: 0.8em;
                color: $third-color-text;
                background-color: $color-second-bg-title;
                border-radius: 50%;
            }
            .icon-arrow {
                position: absolute;
                top:40px;
                right:40px;
                color: $third-color-text;
            }
            h4 {
                font-size: 1.6em;
                margin: 0.5em 0;
            }
        }
    }
}
</style>