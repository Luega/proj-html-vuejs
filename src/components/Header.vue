<template>
<!-- HEADER -->
  <header class="header width-100 flex flex-direction-column">
      <!-- top -->
      <div class="top width-100">
          <div class="container width-60 flex margin-auto justify_content-space-beetween align-items-center">
                <!-- left -->
                <div class="open-hours flex justify_content-center align-items-center">
                    <i class="fas fa-clock clock"></i>
                    <span>Open Hours: {{this.openDays}} - {{this.openHours}}</span>
                </div>
                <!-- right -->
                <div class="contact-info flex align-items-center">
                    <a href="#">
                        <i class="fas fa-phone-alt icon-contact"></i>
                    <span>{{this.phone}}</span>
                    </a>
                    <a href="#">
                        <i class="fas fa-envelope icon-contact"></i>
                    <span>{{this.email}}</span>
                    </a>
                    <a href="#">
                        <i class="fab fa-facebook-f"></i>
                    </a>
                    <a href="#">
                        <i class="fab fa-twitter"></i>
                    </a>
                    <a href="#">
                        <i class="fab fa-linkedin-in"></i>
                    </a>
                </div>
          </div>
      </div>
      <!-- bottom -->
      <div class="width-100">
            <div class="bottom width-60 flex margin-auto justify_content-space-beetween align-items-center">
                <!-- left -->
                <h1 class="h1">
                        <span class="color-logo">NEX</span>
                        <span> GEN</span>
                </h1>
                <!-- right -->
                <nav class="nav flex align-items-center">
                    <ul>
                        <li v-for="(option, index) in navbarElements" :key="index">
                            <a href="#">{{ option }}</a>
                        </li>
                    </ul>
                    <i class="far fa-user user"></i>
                    <button class="button">GET IN TOUCH</button>
                </nav>
            </div>
      </div>
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
    position: absolute;
    top: 0;
    left: 0;
    // top
    .top {
        padding: 0.5em;
        color: $second-color-text;
        background-color: $color-bg-top-header;
        // left
        .clock {
            margin-right: 0.5em;
        }
        // right
        .contact-info {
            a {
                margin-right: 2em;
                color: $second-color-text;
                text-decoration: none;
                .icon-contact {
                    margin-right: 0.5em;
                }
            }
        }
    }
    // bottom
    .bottom {
        padding: 1.5em 0;
        h1 {
            font-size: 1.5em;
            .color-logo {
                    padding: 0.3em 0.3em 0.3em 1em;
                    border-radius: 50px 0 0 50px;
                    color: $third-color-text;
                    background-color: $color-second-bg-title;
                }
        }
        .nav {
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