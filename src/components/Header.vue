<template>
<!-- HEADER -->
  <header class="header width-100 flex flex-direction-column">
      <!-- top -->
      <div class="top width-100 flex">
          <!-- left -->
          <div class="open-hours flex justify_content-center align-items-center">
              <font-awesome-icon class="clock" :icon="['fas', 'clock']"/>
              <span>Open Hours: {{this.openDays}} - {{this.openHours}}</span>
          </div>
          <!-- right -->
          <div class="contact-info flex align-items-center">
              <a href="#">
                  <font-awesome-icon class="phone" :icon="['fas', 'phone-alt']"/>
              <span>{{this.phone}}</span>
              </a>
              <a href="#">
                  <font-awesome-icon class="envelope" :icon="['fas', 'envelope']"/>
              <span>{{this.email}}</span>
              </a>
              <a href="#">
                  <font-awesome-icon :icon="['fas', 'user']"/>
              </a>
              <a href="#">
                  <font-awesome-icon :icon="['fas', 'user']"/>
              </a>
              <a href="#">
                  <font-awesome-icon :icon="['fas', 'user']"/>
              </a>
          </div>
      </div>
      <!-- bottom -->
      <nav class="bottom width-100 flex">
          <!-- left -->
          <div class="company-name flex justify_content-center align-items-center">
              <h1 class="first-part-company-name">NEX</h1>
              <h1 class="second-part-company-name">GEN</h1>
          </div>
          <!-- right -->
          <nav class="nav flex align-items-center">
              <ul>
                  <li v-for="(option, index) in navbarElements" :key="index">
                      <a href="#">{{ option }}</a>
                  </li>
              </ul>
              <font-awesome-icon class="user" :icon="['fas', 'user']"/>
              <button class="button">GET IN TOUCH</button>
          </nav>
      </nav>
  </header>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            openDays: "Mon-Sat",
            openHours: "9:00-18:00",
            phone: "+1(305) 1234-5678",
            email: "hello@example.com",
            navbarElements: ["home", "about", "services", "process", "testimonials"],
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/partials/_common.scss";
@import "../assets/partials/_mixin.scss";
@import "../assets/partials/_variables.scss";


// HEADER
.header {
    height: $header-height;
    position: fixed;
    top: 0;
    left: 0;
    // top
    .top {
        height: 30%;
        color: $second-color-text;
        background-color: $color-bg-top-header;
        // left
        .clock {
            margin-right: 0.5em;
        }
        .open-hours {
            width: 50%;
        }
        // right
        .contact-info {
            width: 50%;
            a {
                margin-right: 2em;
                color: $second-color-text;
                text-decoration: none;
                .phone,
                .envelope {
                    margin-right: 0.5em;
                }
            }
        }
    }
    // bottom
    .bottom {
        height: 70%;
        .company-name {
            width: 40%;
        }
        .nav {
            width: 60%;
            ul {
                @include list-nav;
                li {
                    margin-right: 2em;
                    a {
                        text-transform: uppercase;
                    }
                }
            }
            .user {
                margin-right: 2em;
                cursor: pointer;
            }
            .button {
                @include button-with-bg;
                cursor: pointer;
            }
        }
    }
}

</style>