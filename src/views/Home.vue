<template>
  <div class="wrapper">
    <nav class="main-nav">
      <Profile />
    </nav>
    <article class="content">
      <ProjectLinks />
    </article>
  </div>
</template>

<script>
import ProjectLinks from '@/components/ProjectLinks.vue';
import Profile from '@/components/Profile.vue';

export default {
  name: 'home',
  components: {
    ProjectLinks,
    Profile,
  },
};
</script>
<style scoped>
.content {
  grid-area: content;
  padding: 10px 20px;
  overflow: auto;
}
.main-nav {
  grid-area: nav;
  background-color: rgb(68, 75, 84);
  /* height: 100vh; */
}
.wrapper {
  /* height: 100vh; */
  /* overflow: hidden; */
  display: grid;
  grid-gap: 0px;
  grid-template-areas:
    "nav"
    "content";
}

@media (min-width: 700px) {
  .wrapper {
    grid-template-columns: 1fr 4fr;
    grid-template-areas: "nav    content";
  }
  nav, .wrapper {
    height: 100vh;
  }
  nav ul {
    flex-direction: column;
  }
}
</style>
