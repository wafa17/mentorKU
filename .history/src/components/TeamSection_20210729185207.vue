<template>
  <section id="team">
    <v-container>
      <v-row align="center" justify="center">
        <v-col cols="24">
          <v-row align="center" justify="space-around">
            <v-col cols="12" class="text-center">
              <h1 class="fontstyle font-weight-bold">Meet Our Team</h1>
              <!-- <h1 class="font-weight-light">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </h1> -->
            </v-col >
            <v-col>
            <v-row
              align="center" justify= "center">
              <v-col class="text-center">
                 <v-img
                    src="@/assets/img/fadhil.png"
                    height="auto"
                    max-width="150px"
                    class="d-block ml-auto mr-auto"
                  ></v-img>
                <h2 class="font-weight-normal"> Fadhil Ramadhan </h2>
                <p class="font-weight-light"> Chief Executive Officer </p>
              </v-col>
              <v-col class="text-center">
                <v-img
                        src="@/assets/img/pradhana.png"
                        class=" d-block ml-auto mr-auto"
                        height="auto"
                        max-width="150px"
                      />
                <h2 class="font-weight-normal">Pradhana Ryan</h2>
                <p class="font-weight-light"> Chief Marketing Officer </p>
              </v-col>
              
            </v-row>
            <v-row align="center" justify="center">
              <v-col class="text-center">
                <v-img
                        src="@/assets/img/wafa.png"
                        class=" d-block ml-auto mr-auto"
                        height="auto"
                        max-width="150px"
                      />
                
                <h2 class="font-weight-normal">Wafa Zahida</h2>
                <p class="font-weight-light"> Chief Technology Officer </p>
              </v-col>
              <v-col class="text-center">
                 <v-img
                        src="@/assets/img/dira.png"
                        class=" d-block ml-auto mr-auto"
                        height="auto"
                        max-width="150px"
                      />
                <h2 class="font-weight-normal"> Dira Shafa </h2>
                <p class="font-weight-light"> Designer </p>
              </v-col>
              <v-col class="text-center">
                <v-img
                        src="@/assets/img/earlene.png"
                        class=" d-block ml-auto mr-auto"
                        height="auto"
                        max-width="150px"
                      />
                <h2 class="font-weight-normal"> Earlene Benedicta </h2>
                <p class="font-weight-light"> Designer </p>
              </v-col>
            </v-row>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      videoId: "i8IvvHJssWE",
      features: [
        {
          img: require("@/assets/img/icon2.png"),
          title: "Fadhil Ramadhan",
          text: "Chief Executive Officer",
        },
        {
          img: require("@/assets/img/icon2.png"),
          title: "Pradhana Ryan",
          text: "Chief Marketing Officer",
        },
        {
          img: require("@/assets/img/icon2.png"),
          title: "Wafa Zahida",
          text: "Chief Technology Officer",
        },
        {
          img: require("@/assets/img/icon2.png"),
          title: "Dira Shafa",
          text: "Designer",
        },
        {
          img: require("@/assets/img/icon2.png"),
          title: "Earlene B.G.S.R ",
          text: "Designer",
        },
      ],
    };
  },
  watch: {
    dialog(value) {
      if (!value) {
        this.pause();
      }
    },
  },
  methods: {
    ready(event) {
      this.player = event.target;
    },
    playing(event) {
      // The player is playing a video.
    },
    change() {
      // when you change the value, the player will also change.
      // If you would like to change `playerVars`, please change it before you change `videoId`.
      // If `playerVars.autoplay` is 1, `loadVideoById` will be called.
      // If `playerVars.autoplay` is 0, `cueVideoById` will be called.
      this.videoId = "another video id";
    },
    stop() {
      this.player.stopVideo();
    },
    pause() {
      this.player.pauseVideo();
    },
  },
};
</script>

<style lang="scss">
.circle {
  stroke-dasharray: 650;
  stroke-dashoffset: 650;
  -webkit-transition: all 0.5s ease-in-out;
  opacity: 0.3;
}

.playBut {
  /*  border: 1px solid red;*/
  display: inline-block;
  -webkit-transition: all 0.5s ease;

  .triangle {
    -webkit-transition: all 0.7s ease-in-out;
    stroke-dasharray: 240;
    stroke-dashoffset: 480;
    transform: translateY(0);
  }

  &:hover {
    .triangle {
      stroke-dashoffset: 0;
      opacity: 1;
      animation: nudge 0.7s ease-in-out;

      @keyframes nudge {
        0% {
          transform: translateX(0);
        }
        30% {
          transform: translateX(-5px);
        }
        50% {
          transform: translateX(5px);
        }
        70% {
          transform: translateX(-2px);
        }
        100% {
          transform: translateX(0);
        }
      }
    }

    .circle {
      stroke-dashoffset: 0;
      opacity: 1;
    }
  }
}
</style>

<style>
.btn-play {
  transition: 0.2s;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}

#team {
  z-index: 0;
  font-family: "Poppins";
  background-color: #f8f8f8;
}

.fontstyle {
  font-size: 34px;
}
.svg-border-waves img {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  margin-bottom: -2px;
  z-index: -1;
}

.card {
  min-height: 250px;
  padding: 20px;
  transition: 0.5s ease-out;
}

.card .v-image {
  margin-bottom: 20px;
  transition: 0.75s;
}

.card h1 {
  margin-bottom: 10px;
}

.zoom-efect {
  transform: scale(1.1);
}

.up {
  transform: translateY(-20px);
  transition: 0.5s ease-out;
}

.mainfont {
  font-size: 50px;
  font-weight: bold;
}



/* .v-parallax__image {
 width: 100% !important;
 /* transform: none !important; */
/* height: 100% !important; */
/* } */
</style>

<style>
section {
  position: relative;
}
</style>
