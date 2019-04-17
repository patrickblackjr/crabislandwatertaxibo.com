<template>
<div id="home">
  <b-container>
    <b-carousel 
      id="carousel1"
      class="mt-2 mb-5"
      style="text-shadow: 1px 1px 2px #333;"
      controls
      indicators
      background="#ababab"
      :interval="4000"
      img-width="1024"
      img-height="480"
      v-model="slide"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide img-src="./slides/slide1.jpg"></b-carousel-slide>
      <b-carousel-slide img-src="./slides/slide2.jpg"></b-carousel-slide>
      <b-carousel-slide img-src="./slides/slide3.jpg"></b-carousel-slide>
      <b-carousel-slide img-src="./slides/slide4.jpg"></b-carousel-slide>
    </b-carousel>
  </b-container>
  <b-container>
    <b-row>
      <Boxes
        v-for="box in boxes"
        v-bind:key="box.title"
        :title="box.title"
        :text="box.text"
        :link="box.link" />
    </b-row>
  </b-container>
  <Section 
    v-for="section in section"
    v-bind:key="section.title"
    :title="section.title"
    :text="section.text"
    />
  <WhyUs />
</div>
</template>

<script>
import Boxes   from   '@/components/Boxes.vue';
import Section from   '@/components/Section.vue';
import WhyUs   from   '@/components/WhyUs.vue'

export default {
  components: {
    Boxes,
    Section,
    WhyUs
  },
  head () {
    let title = this.pageTitle;
    return {
      title: title,
      meta: [{
          hid: `description`,
          name: 'description',
          content: `Precision Firestopping excels in all forms of firestopping in commercial construction. Our goal is to provide performance, product, and service that will consistently exceed our client expectations.`
        }
      ],
      __dangerouslyDisableSanitizers: ['script'],
      script: [{ innerHTML: JSON.stringify(this.structuredData), type: 'application/ld+json' }]
    }
  },
  data () {
    return {
      structuredData: {
        "@context" : "http://schema.org",
        "@type" : "LocalBusiness",
        "name" : "Precision Firestopping",
        "image" : "https://d33wubrfki0l68.cloudfront.net/25332a4116a4d6f8b2dc8d6e16148f0053a154fa/4a0c2/_nuxt/img/3a76ada.png",
        "telephone" : "850.897.0240",
        "email" : "brannan@precisionfirestopping.com",
        "url" : "https://precisionfirestopping.com/"
      },
      pageTitle: 'Home',
      slide: 0,
      sliding: null,
      boxes: [
        {
          title: 'Fire Stopping',
          text: 'How does it work?',
          link: '/firestopping'
        },
        {
          title: 'Our Services',
          text: 'Full range of firestopping',
          link: '/services'
        },
        {
          title: 'Bid Request',
          text: 'Inexpensive peace of mind',
          link: '/bid-request'
        },
      ],
      section: [
        {
          title: 'What is firestopping?',
          text: `Firestopping in simple terms is the sealing walls, floors, and ceiling and using products that stop combustion in order to make fire rated walls that stop the spread of fire. Techniques and materials used for firestopping have be tested and approved specifically for this use. The technique of firestopping is a process that takes expertise in the area of fire prevention and is something that your general contractor can't provide. You need a specialized firestopping contractor and Precision Firestopping can provide this service to you.\nPrecision Firestopping excels in all forms of firestopping in commercial construction. Our goal is to provide performance, product, and service that will consistently exceed our client expectations. We have extensive knowledge and experience in working with general contractors as well as sub contractors. In the area of commercial construction, we specialize in firestopping, acoustical sealants, waterproofing and all your caulking needs. You will save time and money by letting us navigate this process for you.`
        },
        {
          title: 'Expect the best.',
          text: `With Precision Firestopping, you can expect the best. We take pride in our work and we send all of our employees through extensive training for the installation of firestop products.
                Do you have a firestop sub contractor to assist you with your projects?
                Are you having problems spending too much money on firestopping or passing your inspections?
                Whatever the problem might be when it comes to firestopping or any other sealants, we do it right!
                We are a specialty trade contractor specializing in the field of commercial firestopping, acoustical sealing, waterproofing, and caulking.`
        }
      ]
    }
  },
  methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    }
  }
}
</script>

<style>

</style>
