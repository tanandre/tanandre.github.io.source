<template>
  <div class="links">
    <p>Welcome to my home page. In case you are interested in one of my projects please click the links below.</p>
    <h3>My projects:</h3>
    <a v-for="link in links" :key="link.url" :href="link.url">
      <div class="link">{{link.name}}</div>
    </a>
  </div>
</template>

<script>
const links = [
  {
    name: 'Planning Poker (Vue+Socket.io)',
    url: 'http://planningpoker-bb.herokuapp.com/',
  },
  {
    name: 'Memori Game (Vue)',
    url: 'https://webmemori.netlify.app/',
  },
  {
    name: 'String Tools (Vue)',
    url: 'https://stringtools.netlify.app/',
  },
  {
    name: 'Avatar Generator (Vue+SVG)',
    url: 'https://avatar-generator.netlify.app/',
  },
  {
    name: 'Web XSLT Processor (React)',
    url: 'https://webxslt.netlify.app/',
  },
  {
    name: 'Flight Tracker (Vue + GMaps)',
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
  width: 300px;
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
