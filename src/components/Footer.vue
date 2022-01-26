<template>
  <footer class="footer container width-100 flex flex-direction-column">
      <div class="width-60 margin-auto flex">
          <!-- top -->
          <!-- left -->
          <div class="contacts">
              <h1 class="h1">
                  <span class="color-logo">NEX</span>
                  <span> GEN</span>
              </h1>
              <p>A functional HTML template for corporate &#38; Business</p>
              <div class="contact-info flex flex-direction-column">
                  <a href="#">
                      <font-awesome-icon class="icon-contact" :icon="['fas', 'phone-alt']"/>
                      <span>{{this.phone}}</span>
                  </a>
                  <a href="#">
                      <font-awesome-icon class="icon-contact" :icon="['fas', 'envelope']"/>
                      <span>{{this.email}}</span>
                  </a>
                  <a href="#">
                      <font-awesome-icon class="icon-contact" :icon="['fas', 'envelope']"/>
                      <span>{{this.email}}</span>
                  </a>
                  <button class="button-with-border">get in touch</button>
             </div>
          </div>
          <!-- right -->
          <div class="box-menu flex">
                <div class="menu flex flex-direction-column justify_content-center" v-for="(menu, index) in menus" :key="index">
                    <h3>{{ menu.title }}</h3>
                    <ul>
                        <li>
                            <a href="#">
                                <font-awesome-icon class="icon-list" :icon="['fas', 'user']"/>
                                <span>{{ menu.lists[0] }}</span>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <font-awesome-icon class="icon-list" :icon="['fas', 'user']"/>
                                <span>{{ menu.lists[1] }}</span>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <font-awesome-icon class="icon-list" :icon="['fas', 'user']"/>
                                <span>{{ menu.lists[2] }}</span>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <font-awesome-icon class="icon-list" :icon="['fas', 'user']"/>
                                <span>{{ menu.lists[3] }}</span>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <font-awesome-icon class="icon-list" :icon="['fas', 'user']"/>
                                <span>{{ menu.lists[4] }}</span>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <font-awesome-icon class="icon-list" :icon="['fas', 'user']"/>
                                <span>{{ menu.lists[5] }}</span>
                            </a>
                        </li>
                    </ul>
                </div>
          </div>
      </div>
      <!-- bottom -->
      <div class="bottom width-100 flex align-items-center">
          <div class="width-60 flex margin-auto justify_content-space-beetween">
                <span>Enjoy the low price. We are tracking any intention of piracy.</span>
                <span>&#169;2020 NEXGEN is Proudly Powered by <a class="green-link" href="#">Codings</a>.</span>
          </div>
          <a href="#"><font-awesome-icon class="icon-top" :icon="['fas', 'user']"/></a>  
      </div>
  </footer>
</template>

<script>
export default {
    name:"Footer",
    data() {
        return {
            menus: [
                {
                    title: "About",
                    lists: ["The Company", "The Company", "The Company", "The Company", "The Company", "The Company"]
                },
                {
                    title: "koior",
                    lists: ["Ciaso", "Ciaso", "Ciaso", "Ciaso", "Ciaso", "Ciaso"]
                },
                {
                    title: "Abofdsafut",
                    lists: ["fgyh", "fgyh", "fgyh", "fgyh", "fgyh", "fgyh"]
                },
            ],
            phone: "+1(305) 1234-5678",
            email: "hello@example.com",
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
    background: linear-gradient($second-color-bg-section , #19191d);
    // top
    // left
    .contacts {
        width: 30%;
        h1 {
            .color-logo {
                padding: 0.3em 0.3em 0.3em 1em;
                border-radius: 50px 0 0 50px;
                color: $third-color-text;
                background-color: $color-second-bg-title;
            }
        }
        p {
            margin: 2em 0;
        }
        a {
            margin-bottom: 1em;
            color: $second-color-text;
            text-decoration: none;
            .icon-contact {
                margin-right: 0.5em;
            }
        }
        button {
            margin-top: 1em;
            width: 60%;
        }
    }
    // right
    .box-menu {
        width: 70%;
        .menu {
            width: calc(100% / 3);
            margin-right: 20px;
            padding: 0 2em;
            color: $second-color-text;
            background-color: $color-bg-card;
            border-radius: 10px;
            h3 {
                margin-bottom: 1em;
                color: $first-color-text;
            }
            ul {
                @include reset-list;
                li {
                    margin: 0.5em 0;
                    a {
                        color: $second-color-text;
                        .icon-list {
                            margin-right: 0.5em;
                        }
                    }
                }
            }
        }
    }
    // bottom
    .bottom {
        height: 80px;
        background-color: $second-color-bg-section;
        span {
            width: 45%;
            text-align: center;
            display: inline-block;
            .green-link {
                color: $third-color-text;
                text-decoration: none;
            }
        }
        .icon-top {
            width: 40px;
            height: 40px;
            padding: 0.5em;
            margin-right: 1em;
            color: $second-color-bg-section;
            background-color: $color-bg-card;
            border-radius: 50%;
        }
    }
}
</style>