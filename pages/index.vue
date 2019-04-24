<template>
  <div id="main">
    <Hero />
    <Rates />
    <About />
    <Contact />
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue';
import Rates from '@/components/Rates.vue';
import About from '@/components/About.vue';
import Contact from '@/components/Contact.vue';

export default {
  components: {
    Hero,
    Rates,
    About,
    Contact
  },
  head() {
    let title = this.pageTitle;
    return {
      title: title,
      meta: [
        {
          hid: `description`,
          name: 'description',
          content: `Bo's Crab Island Water Taxi is the best bang for your buck on the Emerald Coast for ferry and water taxi services to Crab Island.`
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
          streetAddress: '30 State Highway',
          addressLocality: 'Destin',
          addressRegion: 'FL',
          postalCode: '32541'
        },
        image:
          'https://cdn.pixabay.com/photo/2015/08/17/00/07/pontoon-891835_1280.jpg',
        email: 'crabislandwatertaxibo@yahoo.com',
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
          latitude: '30.3911221,',
          longitude: '-86.5222076'
        },
        priceRange: '$$'
      },
      pageTitle: 'Home'
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

<style lang="scss">
#home {
  position: relative;
}
</style>
