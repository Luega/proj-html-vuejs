<template>
  <div>
      <!-- SECTION-1 -->
      <section class="section-story width-100 flex">
          <div class="box-comany-story width-60 flex margin-auto">
              <!-- left -->
              <div class="story">
                  <h3 class="h3">WHO WE ARE</h3>
                  <h2 class="h2">
                      <span class="color"><i class="far fa-gem"></i>Excellence</span>
                      <span> in Transport</span>
                  </h2>
                  <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. A odio delectus eaque laborum cumque magni, in repudiandae minus eius facilis maxime. Ut deleniti rerum sed maiores nemo blanditiis atque voluptatem.</p>
                  <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur, autem quas? Tempore tempora, maxime consectetur qui eaque corporis cumque dicta repellendus error dolore perferendis pariatur. Incidunt et enim eum iusto!</p>
                  <p class="note">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit enim quasi consequuntur sit cupiditate error iure est distinctio harum tempora hic, magnam, quo quisquam. Ratione harum rem corrupti nobis magnam.</p>
                  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique, repellendus voluptatum dolore</p>
                  <div class="box-list">
                    <ul>
                        <li>Lorem ipsum dolor sit amet consectetur .</li>
                        <li>adipisicing elit. Quas, quia nostrum</li>
                        <li>ate magni consequuntur off</li>
                        <li>elit. Quas, quia nostrum adipisicing </li>
                        <li>sicing elit. Quas, quia nostrum adipisic</li>
                    </ul>
                  </div>
              </div>
              <!-- right -->
              <div class="vehicle-certification flex flex-direction-column">
                  <!-- vehicles -->
                  <div class="vehicles">
                    <h4>Vehicle Types</h4>
                    <div class="vehicle flex" v-for="(vehicle, index) in vehicles" :key="index">
                        <img :src="require('../assets/img/truck-1.png')" :alt="vehicle.type">
                        <div class="description">
                            <h5>{{ vehicle.type }}</h5>
                            <span>{{ vehicle.cargo }}</span>
                        </div>
                    </div>
                  </div>
                  <!-- certifications -->
                  <div class="certifications">
                    <h4>Certifications</h4>
                    <img src="../assets/img/certificate.png" alt="certificate">
                    <img src="../assets/img/certificate.png" alt="certificate">
                  </div>
              </div>
          </div>
      </section>
  </div>
</template>

<script>
export default {
    name:"SectionStory",
    data() {
        return {
            vehicles: [
                {
                    img: "../assets/img/truck-1.png",
                    type: "Light",
                    cargo: "Max Weight 1200 kg"
                },
                {
                    img: "../assets/img/truck-1.png",
                    type: "Medium",
                    cargo: "Max Weight 6000 kg"
                },
                {
                    img: "../assets/img/truck-1.png",
                    type: "Heavy",
                    cargo: "Max Weight 24000 kg"
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/partials/_common.scss";
@import "../assets/partials/_mixin.scss";
@import "../assets/partials/_variables.scss";

// SECTION-1
.section-story {
    height: 100vh;
    background-color: $first-color-bg-section;
    // left
    .story {
        width: 70%;
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
            &.note {
                padding: 1em;
                border-left: 5px solid $color-bg-title;
                font-style: oblique;
            }
        }
        .box-list {
            padding: 0 1em;
        }
    }
}
    // right
    .vehicle-certification {
        width: 30%;
        margin-left: 4em;
        color: $second-color-text;
        // vehicles
        h4 {
            margin-bottom: 1em;
            color: $fourth-color-text;
            font-size: 1.5em;
        }
        .vehicle {
            padding: 0.5em 0;
            border-bottom: 1px solid $second-color-text;
            img {
                width: 80px;
                height: auto;
                padding: 0.5em;
                margin-right: 1em;
                background-color: $color-bg-title;
                border-radius: 5px;
            }
            h5 {
                color: $fourth-color-text;
                font-size: 1.5em;
            }
            
        }
        // certifications
        .certifications {
            margin-top: 2em;
            h4 {
                margin-bottom: 0.5em;
            }
            img {
                width: 100px;
                height: auto;
                margin-right: 1em;
                box-shadow: 0px 0px 5px rgb(223, 222, 222); 
            }
        }
    }
</style>