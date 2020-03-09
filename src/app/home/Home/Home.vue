<template>
  <div>
    <stage :disable-particles="disableParticles" />
    <home-section
      image="https://images.unsplash.com/photo-1549082984-1323b94df9a6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=512&q=60"
      alternative
    >
      <vue-headline level="2">About Us</vue-headline>
      <br />
      <vue-headline level="3">Quality Guaranteed</vue-headline>
      <p>We work around the clock and don't stop until your app is delivered!</p>
      <br />
      <vue-headline level="3">Lightspeed ahead!</vue-headline>
      <p>
        We develop applications at lightning speeds! Need to get something up and running by next month? 
        Check out the plethora of options we provide to get exactly what you need, when you need it!
      </p>
      <br />
      <vue-headline level="3">Testomonials</vue-headline>
      <p>
        "Roman's Creations provides top notch service, hands down would hire them again!" - Awesome Client
      </p>
    </home-section>

    <home-section
      image="https://images.unsplash.com/photo-1521790361543-f645cf042ec4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=512&q=60"
      flip
    >
      <vue-headline level="2">Enterprise ready</vue-headline>
      <br />
      <vue-headline level="3">SEO</vue-headline>
      <p>
        Ready to tackle all your SEO needs to get you to the top of the search results. I can work with different solutions to get you up and running how you need.
        Whether it's a PWA or some other type of website or app, I will assess your needs to make the right decision to get the job done.
      </p>
      <br />
      <vue-headline level="3">Best practices</vue-headline>
      <p>
        I am always committed to implementing the best practices to all the solutions I provide. I keep things as simple as possible and even if I begin with a boilerplate, I always end with something to call my own.
      </p>
      <br />
      <vue-headline level="3">Accessible</vue-headline>
      <p>
        I will always go out of my way to make sure that my apps and websites are accessible to everyone who visits. 
        I enjoy staying up to date on what the best practices are and always want to provide the best user experience upon every visit!
      </p>
    </home-section>

    <home-section
      image="https://images.unsplash.com/photo-1543286386-713bdd548da4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=512&q=60"
      alternative
    >
      <vue-headline level="2">User experience</vue-headline>
      <br />
      <vue-headline level="3">Animations</vue-headline>
      <p>
       
      </p>
      <br />
      <vue-headline level="3">Progressive-Web-App</vue-headline>
      <p>
        
      </p>
      <br />
      <vue-headline level="3">Design System</vue-headline>
      <p>
       
      </p>
    </home-section>

    <home-section
      image="https://images.unsplash.com/photo-1516381548400-349d680edb56?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=512&q=60"
      flip
    >
      <vue-headline level="2">Simple Solutions</vue-headline>
      <br />
      <vue-headline level="3">We focus on building the simplest solution possible for your specific situation and needs.</vue-headline>
      <br />
      <vue-headline level="4"> I have some simple rules I always like to follow to make sure your app is in tip top shape.</vue-headline>
      <br />
      <ol>
        <li>
          Your app should run pretty much anywhere, I make sure it will<br />
        </li>
        <li>Your project should be accessible and always use best practices</li>
        <li>Your apps codebase should be easy to understand and never overcomplicated</li>
      </ol>
    </home-section>
  </div>
</template>

<script lang="ts">
import { mapState } from 'vuex';
import Stage from '../components/Stage/Stage.vue';
import HomeSection from '@/app/home/components/HomeSection/HomeSection.vue';
import { IState } from '@/app/state';
import VueHeadline from '@components/VueHeadline/VueHeadline.vue';

export default {
  metaInfo: {
    title: 'vuesion - flexible, scalable, opinionated, fast',
    meta: [
      {
        name: 'description',
        content:
          'vuesion - The most complete boilerplate for production-ready PWAs. With focus on performance, development speed, and best practices',
      },
      {
        name: 'robots',
        content: 'INDEX,FOLLOW',
      },
      {
        name: 'keywords',
        content: 'vue.js, vuex, vuex-persist, seo, server-side-rendering, isomorphic, progressive-web-app',
      },

      { name: 'og:url', content: 'https://vuesion.herokuapp.com/' },
      { name: 'og:site_name', content: 'vuesion' },
      { name: 'og:type', content: 'website' },
      { name: 'og:locale', content: 'en' },
      {
        name: 'og:title',
        content:
          'vuesion - The most complete boilerplate for production-ready PWAs. With focus on performance, development speed, and best practices',
      },
      {
        name: 'og:description',
        content:
          'vuesion - The most complete boilerplate for production-ready PWAs. With focus on performance, development speed, and best practices',
      },
      { name: 'og:image:url', content: 'https://vuesion.herokuapp.com/logo.png' },

      { name: 'twitter:card', content: 'summary' },
      { name: 'twitter:site', content: '@vuesion1' },
      { name: 'twitter:creator', content: '@vuesion1' },
      {
        name: 'twitter:title',
        content:
          'vuesion - The most complete boilerplate for production-ready PWAs. With focus on performance, development speed, and best practices',
      },
      { name: 'twitter:url', content: 'https://vuesion.herokuapp.com/' },
      { name: 'twitter:image', content: 'https://vuesion.herokuapp.com/logo.png' },
      {
        name: 'twitter:description',
        content:
          'vuesion - The most complete boilerplate for production-ready PWAs. With focus on performance, development speed, and best practices',
      },
    ],
  },
  components: {
    VueHeadline,
    HomeSection,
    Stage,
  },
  computed: {
    ...mapState({
      disableParticles: (state: IState) =>
        (state.app.config && state.app.config.features && state.app.config.features.disableParticles) || false,
    }),
  },
};
</script>
