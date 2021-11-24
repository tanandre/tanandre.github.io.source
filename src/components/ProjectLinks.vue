<template>
  <div class="links">
    <p>
      Welcome to my home page. In case you are interested in one of my projects
      please click the links below.
    </p>
    <h3>My projects:</h3>
    <div class="container">
      <Card :link="link" v-for="link in links" :key="link.url" />
    </div>
  </div>
</template>

<script>
import Card from './Card.vue';

const links = [
  {
    name: 'Planning Poker (Vue+Socket.io)',
    img: 'planningpoker.png',
    summary:
      'Use with my team to do sprint planning. WebSockets are used to sync the data between the different browser sessions',
    url: 'http://planningpoker-bb.herokuapp.com/',
  },
  {
    name: 'Memori Game (Vue)',
    img: 'webmemori.png',
    summary: 'A simple memory game to entertain my kids with.',
    url: 'https://webmemori.netlify.app/',
  },
  {
    name: 'PhotoIndex (Vue+PHP)',
    img: 'photoindex.png',
    summary:
      'A Synology photo album app for personal use. Allows for easy searching/tagging of photos and using routing to determine state which results in proper backbutton support. Note the demo uses a mock back-end and only the query functionality works,',
    url: 'https://photoindex-demo.netlify.app',
  },
  {
    name: 'String Tools (Vue)',
    img: 'stringtools.png',
    summary: 'Convenient String manipulation tools that I often use',
    url: 'https://stringtools.netlify.app/',
  },
  {
    name: 'Avatar Generator (Vue+SVG)',
    img: 'avatargen.png',
    summary: 'Creating random avatars for a game I want to build',
    url: 'https://avatar-generator.netlify.app/',
  },
  {
    name: 'Web XSLT Processor (React)',
    img: 'webxslt.png',
    summary: 'A tool to easily test XSLT scripts',
    url: 'https://webxslt.netlify.app/',
  },
  {
    name: 'Flight Tracker (Vue + GMaps)',
    img: 'flighttracker.jpg',
    summary: 'Showing the current airplanes on a map using available open APIs',
    url: 'https://flight-tracker.netlify.app/',
  },
];

export default {
  components: { Card },
  data() {
    return {
      links,
    };
  },
};
</script>
<style scoped>
.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-gap: 20px;
}
</style>
