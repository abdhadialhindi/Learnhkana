<template>
  <div>
    <slider></slider>
    <!-- <business></business> -->
    <service></service>
    <our-work></our-work>
    <experts></experts>
    <testimonial></testimonial>
    <client></client>
    <brand></brand>
    <about></about>
    <news></news>
    <strategic-partner></strategic-partner>
    <!-- <experince1></experince1> -->
    <!-- <experince2></experince2> -->
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      // title: this.title,
      description: `Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet`,
      image: "/bg-image-16-oo.jpg"
    };
  },
  computed:{
    title() {
      return this.$t("About Us")
    }
  },
  head() {

    return {
      title: this.title,
      description: this.description,
      link: [
        {
          rel: 'canonical',
          href: 'https://frolicking-platypus-67395f.netlify.app/',
          hid: 'canonical'
        },
      ],
      htmlAttrs: {
        lang: this.$i18n.locale
      },
      meta: [

      { charset: "utf-8" },
      { name: "viewport", content: "width=device-width, initial-scale=1" },
    {
      hid: 'title',
      name: 'title',
      property: 'og:title',
      content: this.title
    },
        {
          property: 'og:image:width',
          content: '1500',
        },
        {
          property: 'og:image:height',
          content: '1500',
        },
        {
          hid: 'og:title',
          name: 'og:title',
          content: this.title,
        },
        {
          hid: 'description',
          name: 'description',
          content: this.description,
        },
        {
          hid: 'og:description',
          property: 'og:description',
          content: this.description,
        },
        {
          hid: 'og:url',
          property: 'og:url',
          content:'https://frolicking-platypus-67395f.netlify.app/',
        },

        {
          hid: 'og:type',
          property: 'og:type',
          content: 'website',
        },
        {
          hid: 'og:locale',
          property: 'og:locale',
          content: 'en_US',
        },
        {
          hid: 'og:image',
          property: 'og:image',
          content: this.image,
        },
        {
          hid: 'og:image-name',
          name: 'og:image',
          content: this.image,
        },
        {
          hid: 'og:image:secure_url',
          property: 'og:image:secure_url',
          content: this.image,
        },
        {
          hid: 'og:image:alt',
          property: 'og:image:alt',
          content: this.image,
        },
        { hid: 'fb:app_id', name: 'fb:app_id', content: 'different content' },
        {
          hid: 'facebook:pageId',
          name: 'facebook:pageId',
          content: this.title,
        },
        {
          hid: 'facebook:appId',
          name: 'facebook:appId',
          content: this.title,
        },

        {
          hid: 'twitter:title',
          name: 'twitter:title',
          content: this.title,
        },
        {
          hid: 'twitter:card',
          name: 'twitter:card',
          content: 'summary_large_image',
        },
        {
          hid: 'twitter:image',
          name: 'twitter:image',
          content:this.image,
        },
        {
          hid: 'twitter:description',
          name: 'twitter:description',
          content: this.description,
        },
        {
          hid: 'twitter:site',
          name: 'twitter:site',
          content: '@mdotacademy',
        },
        {
          hid: 'twitter:creator',
          name: 'twitter:creator',
          content: '@markshust',
        },
      ],
    }
  }
};
</script>
