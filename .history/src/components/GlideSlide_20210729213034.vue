<template>
  <div>
  <b-container>
    <b-row>
      <b-col cols="12">
        <carousel :perPage="3">
          <slide class="p-2">
            <b-card title="Card Title 1" img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top tag="article">
              <b-card-text>
                Some quick example text to build on the card title and make up the bulk of the card's content.
              </b-card-text>
              <b-button href="#" variant="primary">Go somewhere</b-button>
            </b-card>
          </slide>
          <slide class="p-2">
            <b-card title="Card Title 2" img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top tag="article">
              <b-card-text>
                Some quick example text to build on the card title and make up the bulk of the card's content.
              </b-card-text>

              <b-button href="#" variant="primary">Go somewhere</b-button>
            </b-card>
          </slide>
          <slide class="p-2">
            <b-card title="Card Title 3" img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top tag="article">
              <b-card-text>
                Some quick example text to build on the card title and make up the bulk of the card's content.
              </b-card-text>

              <b-button href="#" variant="primary">Go somewhere</b-button>
            </b-card>
          </slide>
          <slide class="p-2">
            <b-card title="Card Title 4" img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top tag="article">
              <b-card-text>
                Some quick example text to build on the card title and make up the bulk of the card's content.
              </b-card-text>

              <b-button href="#" variant="primary">Go somewhere</b-button>
            </b-card>
          </slide>
        </carousel>
      </b-col>
    </b-row>
  </b-container>
</div>
</template>

<script>
export default {
   data: () => ({
  components: {
    'carousel': VueCarousel.Carousel,
    'slide': VueCarousel.Slide
  },
  
  data: {
    slide: 0,
    sliding: null
  },
  methods: {
        onSlideStart(slide) {
            this.sliding = true
        },
        onSlideEnd(slide) {
            this.sliding = false
        }
  },
})
</script>

<style >
.row{
  margin-top:100px;
}
</style>