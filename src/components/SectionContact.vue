<template>
  <div>
      <section class="section-contact width-100 flex">
          <div class="width-60 flex margin-auto">
              <!-- left -->
              <div class="box-input">
                  <h3 class="h3">SEND A MESSAGE</h3>
                  <h2 class="h2">
                      <span>Get in </span>
                      <span class="color">Touch</span>
                  </h2>
                  <p>We will respond to your message a soon as possible.</p>
                  <form action="#" class="flex">
                      <input class="input-user" type="text" id="name" name="name" placeholder="Name">
                      <input class="input-user" type="email" id="email" name="email" placeholder="Email">
                      <input class="input-user" type="tel" id="phone" name="phone" placeholder="Phone">
                      <select class="input-user" name="info" id="info">
                          <option value="none" selected disabled hidden>More Info</option>
                          <option value="truck">Truck</option>
                          <option value="price">Price</option>
                          <option value="rent">Rent</option>
                      </select>
                      <textarea class="input-user" name="text" id="text" placeholder="Message"></textarea>
                  </form>
                  <button class="button-with-bg">send</button>
              </div>
              <!-- right -->
              <div class="box-contacts">
                    <h4>Example Inc.</h4>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
                    <p>Minus ratione accusantium voluptatibus amet.</p>
                    <div class="contact-info flex flex-direction-column">
                        <a href="#">
                            <i class="fas fa-phone-alt icon-contact"></i>
                            <span>{{this.phone}}</span>
                        </a>
                        <a href="#">
                            <i class="fas fa-envelope icon-contact"></i>
                            <span>{{this.email}}</span>
                        </a>
                        <a href="#">
                            <i class="fas fa-map-marker-alt icon-contact"></i>
                            <span>{{this.position}}</span>
                        </a>
                        <button class="button-with-border">view map</button>
                    </div>
                </div>
          </div>
      </section>
  </div>
</template>

<script>
export default {
    name:"SectionContact",
    data() {
        return {
            phone: "+1(305) 1234-5678",
            email: "hello@example.com",
            position: "Main Avanue, 987"
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/partials/_common.scss";
@import "../assets/partials/_mixin.scss";
@import "../assets/partials/_variables.scss";

.section-contact {
    height: 100vh;
    background-color: $first-color-bg-section;
    // left
    .box-input {
        width: 60%;
        color: $second-color-text;
        h2 {
            color: $fourth-color-text;;
        }
        .color {
            color: $third-color-text;
            background-color: $color-bg-title;
        }
        p {
            margin-bottom: 1.5em;
        }
        form {
            width: 100%;
            flex-wrap: wrap;
            .input-user {
                flex-basis: calc((100% / 2) - 10px);
                margin: 5px;
                padding: 1em;
                border: none;
                background: rgba(236,236,236,255);
                border-radius: 5px;
            }
            #text {
                height: 100px;
                flex-basis: 100%;
                margin-bottom: 2em;
            }

        }
    }
    .box-contacts {
        margin-left: 3em;
        h4 {
            color: $fourth-color-text;
            font-size: 1.5em;
        }
        p {
            margin: 1.5em 0;
        }
        a {
            margin-bottom: 1em;
            color: $third-color-text;
            text-decoration: none;
            .icon-contact {
                width: 30px;
                height: 30px;
                padding: 0.5em;
                margin-right: 1em;
                vertical-align: middle;
                color: $third-color-text;
                background-color: $color-bg-title;
                border-radius: 50%;
            }
        }
        button {
            width: 40%;
            color: $third-color-text;
        }
    }
}
    // right
    
</style>