<template>
  <div id="home">
    <Hero />
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue';

export default {
  components: {
    Hero
  },
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
