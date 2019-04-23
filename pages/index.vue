<template>
  <div id="home">
    <b-carousel
      v-model="slide"
      class="mb-5 d-none d-lg-block"
      style="text-shadow: 1px 1px 1px #333"
      background="#ababab"
      :interval="4000"
      img-width="100%"
      img-height="200"
    >
      <b-carousel-slide img-src="main.jpg">
        <h1>Bo's Crab Island Water Taxi</h1>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  components: {},
  head() {
    let title = this.pageTitle;
    return {
      title: title,
      meta: [
        {
          hid: `description`,
          name: 'description',
          content: `Precision Firestopping excels in all forms of firestopping in commercial construction. Our goal is to provide performance, product, and service that will consistently exceed our client expectations.`
        }
      ],
      __dangerouslyDisableSanitizers: ['script'],
      script: [
        {
          innerHTML: JSON.stringify(this.structuredData),
          type: 'application/ld+json'
        }
      ]
    };
  },
  data() {
    return {
      structuredData: {
        '@context': 'http://schema.org',
        '@type': 'LocalBusiness',
        name: `Bo's Crab Island Water Taxi`,
        address: {
          '@type': 'PostalAddress',
          streetAddress: '285 Harbor Blvd',
          addressLocality: 'Destin',
          addressRegion: 'FL',
          postalCode: '32541'
        },
        image:
          'https://cdn.pixabay.com/photo/2015/08/17/00/07/pontoon-891835_1280.jpg',
        email: 'bigbadbo6969@gmail.com',
        telePhone: '(850) 307-2788',
        url: 'crabislandwatertaxibo.com',
        paymentAccepted: ['cash', 'credit card'],
        openingHours: 'Mo,Tu,We,Th,Fr,Sa 11:00-19:00',
        openingHoursSpecification: [
          {
            '@type': 'OpeningHoursSpecification',
            dayOfWeek: [
              'Monday',
              'Tuesday',
              'Wednesday',
              'Thursday',
              'Friday',
              'Saturday'
            ],
            opens: '11:00',
            closes: '19:00'
          }
        ],
        geo: {
          '@type': 'GeoCoordinates',
          latitude: '30.394763',
          longitude: '-86.505772'
        },
        priceRange: '$$'
      },
      pageTitle: 'Home',
      slide: 0,
      sliding: null
    };
  },
  methods: {
    // Convenience method to scroll a heading into view.
    // Not required for scrollspy to work
    scrollIntoView(evt) {
      evt.preventDefault();
      const href = evt.target.getAttribute('href');
      const el = href ? document.querySelector(href) : null;
      if (el) {
        this.$refs.content.scrollTop = el.offsetTop;
      }
    }
  }
};
</script>
