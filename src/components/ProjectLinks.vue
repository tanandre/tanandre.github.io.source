<template>
  <div class="links">
    <p>
      Welcome to my home page. In case you are interested in one of my projects
      please click the links below.
    </p>
    <h3>My projects:</h3>
    <div class="container">
      <div class="card" v-for="link in links" :key="link.url" :href="link.url">
        <div class="header">{{ link.name }}</div>

        <p class="description">{{ link.summary }}</p>
        <div class="actions">
          <a :href="link.url">demo</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
const links = [
  {
    name: 'Planning Poker (Vue+Socket.io)',
    summary:
      'Use with my team to do sprint planning. WebSockets are used to sync the data between the different browser sessions',
    url: 'http://planningpoker-bb.herokuapp.com/',
  },
  {
    name: 'Memori Game (Vue)',
    summary: 'A simple memory game to entertain my kids with.',
    url: 'https://webmemori.netlify.app/',
  },
  {
    name: 'PhotoIndex (Vue+PHP)',
    summary:
      'A Synology photo album app for personal use. Allows for easy searching/tagging of photos and using routing to determine state which results in proper backbutton support. Note the demo uses a mock back-end and only the query functionality works,',
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
.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  padding: 20px;
  color: rgba(255,255,255, 0.8);
  background-color: rgb(66, 131, 185);
  margin: 5px;
}

.card:hover {
  filter: brightness(120%);
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.8);
}

.card .header {
  font-weight: bold;
  color: rgb(255,255,255);
}

.card .actions {

}

.container {
  display: grid;
  /* grid: 150px / auto auto; */
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-gap: 5px;
}
</style>
