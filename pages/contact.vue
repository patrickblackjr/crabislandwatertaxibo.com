<template>
<div id="home">
  <div class="container mt-3">
    <h1 class="text-center mt-5 mb-5">{{ pageTitle }}</h1>
    <b-breadcrumb :items="items" />
    <b-row>
      <b-col cols="4">
        <h2>Contact Info</h2>
        <p><strong>Thank you for your interest in Precision Firestopping.</strong></p>
        <p>
          We are a family owned and operated company with focus on fire prevention in the 
          commercial industry of all construction. We regularly service the Florida panhandle 
          from Perdido Beach to Tallahasee. We can however perform firestopping projects 
          outside of our specified region. For more information, contact our Sales department 
          or submit a Bid Request.
        </p>
        <h3>Project Management</h3>
        <p><strong>Brannan Burdette</strong></p>
        <p>Office: 850.897.0240</p>
        <p>Cell: 850.240.5651</p>
        <p>Email: <a href="mailto:brannan@precisionfirestopping.com"> brannan@precisionfirestopping.com</a></p>
      </b-col>
      <b-col>
        <h2>Contact Form</h2>
        <p><strong>Please do not submit bit requests here. You can find that <a href="bid-request">here</a>.</strong> Just fill out this form and we'll be in touch.</p>
        <contact-form/>
      </b-col>
    </b-row>
  </div>
</div>
</template>

<script>
import ContactForm from '@/components/ContactForm.vue';

export default {
  components: {
    ContactForm
  },
  head () {
    let title = this.pageTitle;
    return {
      title: title,
      meta: [{
          hid: `description`,
          name: 'description',
          content: `Contact our team today with any questions.`
        }
      ]
    }
  },
  data () {
    return {
      pageTitle: 'Contact',
      items: [
        {
          text: 'Home',
          href: '/'
        },
        {
          text: 'Contact',
          href: '/contact'
        }
      ]
    }
  }
}
</script>

<style>

</style>
