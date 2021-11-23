<template>
  <div class="links">
    <p>Welcome to my home page. In case you are interested in one of my projects please click the links below.</p>
    <h3>My projects:</h3>
    <a v-for="link in links" :key="link.url" :href="link.url">
      <div class="link">{{link.name}}
        <p>{{link.summary}}</p>
      </div>
    </a>
  </div>
</template>

<script>
const links = [
  {
    name: 'Planning Poker (Vue+Socket.io)',
    summary: 'Use with my team to do sprint planning. WebSockets are used to sync the data between the different browser sessions',
    url: 'http://planningpoker-bb.herokuapp.com/',
  },
  {
    name: 'Memori Game (Vue)',
    summary: 'A simple memory game to entertain my kids with.',
    url: 'https://webmemori.netlify.app/',
  },
  {
    name: 'PhotoIndex (Vue+PHP)',
    summary: 'A Synology photo album app for personal use. Allows for easy searching/tagging of photos and using routing to determine state which results in proper backbutton support. Note the demo uses a mock back-end and only the query functionality works,',
    url: 'https://photoindex-demo.netlify.app',
  },
  {
    name: 'String Tools (Vue)',
    summary: 'Convenient String manipulation tools that I often use',
    url: 'https://stringtools.netlify.app/',
  },
  {
    name: 'Avatar Generator (Vue+SVG)',
    summary: 'Creating random avatars for a game I want to build',
    url: 'https://avatar-generator.netlify.app/',
  },
  {
    name: 'Web XSLT Processor (React)',
    summary: 'A tool to easily test XSLT scripts',
    url: 'https://webxslt.netlify.app/',
  },
  {
    name: 'Flight Tracker (Vue + GMaps)',
    summary: 'Showing the current airplanes on a map using available open APIs',
    url: 'https://flight-tracker.netlify.app/',
  },
];

export default {
  data() {
    return {
      links,
    };
  },
};
</script>
<style scoped>
h3 {
  margin: 10px 0;
}
.links {
  width: 70%;
}
a {
  text-decoration: none;
}

.links .link {
  margin: 2px;
  padding: 10px 25px;
  width: 500px;
  color: #fff;
  /* background-color: #61DAFB; */
  background-color: rgb(66, 131, 185);
  transition: 0.3s;
}

.links .link:hover {
  background-color: rgba(66, 131, 185, 0.5);
  /* background-blend-mode: darken; */
}
</style>
